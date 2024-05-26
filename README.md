# SI_2024_lab2_223117
# Живко Коцев 223117
![e0c3634d-6d6e-4d90-ab6a-17923aaf6f42](https://github.com/zhivko-kocev/SI_2024_lab2_223117/assets/116723781/e33ad56a-cf78-4e8b-a8ad-35b4cddace5a)
###Цикломатска комплексност - 10 , преку формуалта P+1 , P е бројот на предикатни јазли. P = 9 , па цикломатска комплексност 10.

Тест случаи според критериумот Every Branch
Test case: allItems=null, payment=100 - 1->2->27,
фрла Exception и излегува од програма

Test case: allItems=[], payment=0 - 1->3->4.1->4.2->23->24->27, празна листа, ќе падне на 4.2 во for циклусот, allItems.size() не е поголемо од i=0, sum<=payment.

Test case: allItems=[], payment=-1 - 1->3->4.1->4.2->23->25->26->27, празна листа, ќе падне на 4.2 во for циклусот, allItems.size() не е поголемо од i=0, sum>payment.

Test case: allItems = [new Item("", "null", 100, 0.1f)], payment = 100 - 1->3->4.1->4.2->5->6->7->8->19->20->27, вредноста за името е празен String, вредноста на index е null

Test case: allItem = [new Item("", "012345", 350, 0.1f)], payment=100 - 1->3->4.1->4.2->5->6->7->8->9->10->11.1->11.2->12->13->11.11.3->11.2->15->16->21->22->4.3->4.2->8->23->25->26->27, баркодот почнува на 0, и цената е над 300.

Test case: allItems = [new Item("Item1", "12345a", 100, 0.1f)], payment = 100 - 1->3->4.1->4.2->5->6->8->9->10->11.1->11.2->12->13->14->27, во овој test case, имаме име и баркодот содржи буква

Test case: allItems = [new Item("Item1", "12345", 100, -1f)], payment = 100 - 1->3->4.1->4.2->5->6->8->9->10->11.1->11.2->12->13->11.1->11.2->15->17->18->21->4.3->4.2->23->24->27, цената е помала од 300, попустот е негативна вредност

Тест случаи според критериумот Multiple Condition
а)350;0.2;12345 - враќа false, TTF

б)350;0;12345 - враќа false, TFF

в)350;0.2;01234 - враќа true, TTT

г)100;0.2;01234 - враќа false FTT
