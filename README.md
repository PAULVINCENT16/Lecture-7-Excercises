# Lecture-7-Excercises
//Slide 16 (Mark my words)

#include using namespace std;

int Display() { int studentGrade = 0; cout << "Enter Student's grade: "; cin >> studentGrade; return studentGrade; }

void markGrade(int Grade) {

if (Grade >= 40 && Grade <= 100) {
	if (Grade >= 70) {
		cout << "Student's mark is: A " << endl;
	}
	else if (Grade >= 60 && Grade <= 69) {
		cout << "Student's mark is: B " << endl;
	}
	else if (Grade >= 50 && Grade <= 59) {
		cout << "Student's mark is: C " << endl;
	}
	else if (Grade >= 40 && Grade <= 49) {
		cout << "Student's mark is: D " << endl;
	}
}else if (Grade >= 101) {
	cout << "TOO MUCH GRADE!!!" << endl;
}
else {
	cout << "Student's mark is: F" << endl;
}
}

int main() {

int studentGrade = 0;
studentGrade = Display();
markGrade(studentGrade);

return 0;
}

//Slide 17 (Starting a Band)

#include using namespace std;

bool stringTest(string ins) { string friendPlaysG = "Guitar", friendPlaysg = "guitar"; string friendPlaysD = "Drums", friendPlaysd = "drums";

if (ins == friendPlaysG || ins == friendPlaysg) {
	return true;
}
else if (ins == friendPlaysD || ins == friendPlaysd || ins == "drum" || ins == "Drum") {
	return true;
}
else {
	return false;
}
} void Display() { char choice; bool musicalFriend = true; string instrument; while (musicalFriend) { cout << "Can you play instrument?\nPress 'y' for yes and Press 'n' for no: "; cin >> choice; system("cls"); if (choice == 'y') { cout << "What instrument do you play?: "; cin >> instrument; if (stringTest(instrument)) { system("cls"); cout << "cool! you're in, since you can play " << instrument; musicalFriend = false; } else { system("cls"); cout << "Sorry we don't need that at the moment" << endl; musicalFriend = false; } } else if (choice == 'n') { cout << "You're not for this" << endl; musicalFriend = false; } else { cout << "It's not in the choices try again" << endl << endl; } } } int main() {

Display();

return 0;
}

//Slide 19 (Killing Time)

#include using namespace std;

void Display() { char firstChoice, secondChoice; bool Friend = true;

while (Friend) {
	cout << "Is your friend going to be with you less than 15 mins?\nPress 'y' for yes and Press 'n' for no: "; cin >> firstChoice;
	system("cls");
	if (firstChoice == 'y') {
		cout << "Sit in the food zone and wait." << endl;
		Friend = false;
	}
	else if (firstChoice == 'n') {
		system("cls");
		cout << "Do you have extra money? more than 5 AED?\nPress 'y' for yes and Press 'n' for no: "; cin >> secondChoice;
		if (secondChoice == 'y') {
			cout << "\ngo buy a drink or snacks" << endl;
			Friend = false;
		}
		else if (secondChoice == 'n') {
			cout << "\ngo for a walk around the town " << endl;
			Friend = false;
		}
		else {
			system("cls");
			cout << "It's not in the choices try again" << endl << endl;
		}
	}
	else {
		cout << "It's not in the choices try again" << endl << endl;
	}
}
}

int main() {

Display();

return 0;
}

//Slide 20 (Earthquake)

#include using namespace std;

int Display() { float Earthquake = 0; cout << "Enter earthquake's magnitude: "; cin >> Earthquake; return Earthquake; }

void MagnitudeTest(float Earthquake) {

if (Earthquake >= 2.0 && Earthquake <= 10.0) {
	
	if (Earthquake <= 10.0 && Earthquake >= 8.0) {
		cout << "The earthquake was Great" << endl;
	}
	else if (Earthquake <= 8.0 && Earthquake >= 7.0) {
		cout << "The earthquake was Major" << endl;
	}
	else if (Earthquake <= 7.0 && Earthquake >= 6.0) {
		cout << "The earthquake was Strong" << endl;
	}
	else if (Earthquake <= 6.0 && Earthquake >= 5.0) {
		cout << "The earthquake was Moderate" << endl;
	}
	else if (Earthquake <= 5.0 && Earthquake >= 4.0) {
		cout << "The earthquake was Light" << endl;
	}
	else if (Earthquake <= 4.0 && Earthquake >= 3.0) {
		cout << "The earthquake was Minor" << endl;
	}
	else if (Earthquake <= 3.0 && Earthquake >= 2.0) {
		cout << "The earthquake was Very Minor" << endl;
	}
}
else if (Earthquake >= 11) {
	cout << "The earthquake was Meteoric" << endl;
}
else {
	cout << "The earthquake was Micro" << endl;
}
}

int main() {

int Earthquake = 0;
Earthquake = Display();
MagnitudeTest(Earthquake);

return 0;
}
