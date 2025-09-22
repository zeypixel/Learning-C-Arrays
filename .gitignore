#include<iostream>
#include<array>
#include<string>

using namespace std;

// function to print array elements
void print_array(array<int, 5>arr) {
	cout << "Array : ";
	for (int element : arr) {
		cout << element << " ";
	}
	cout << "\n";
}

int main() {

	// normal C-style array
	int array1[5] = { 1,2,3,4,5 };
	cout <<"Arrray1 [1] : " << array1[1] << endl;

	// we can change element value by index
	array1[1] = 10;
	cout << "Arrray1 [1] : " << array1[1] << endl;

	// std::array is like normal array but has more functions //
	array <int, 5>array2 = { 1,2,3,4,5 };
	cout << "Arrray2 [1] : " << array2[1] << endl;
	array2[1] = 10;
	cout << "Arrray2 [1] : " << array2[1] << endl;

	// creating array with other values //
	array<int, 5>array3 = { 9,8,7,6,5 };
	cout << "array[1] : " << array3[1] << endl;

	// array[i] == array.at(i) but at() checks range //
	cout << "array.at(2) : " << array3.at(2) << endl;

	// array.front() gives first element //
	// array.back() gives last element //
	cout << "array3.front() : " << array3.front() << endl;
	cout << "array3.back() : " << array3.back() << endl;

	// size() gives number of elements //
	// max_size() is same as size() in std::array //
	cout << "array.size() : " << array3.size() << endl;
	cout << "array.max_size() : " << array3.max_size() << endl;

	// print all elements with for loop //
	for (int i = 0; i < array3.size(); i++) {
		cout << "array3[" << i << "] : " << array3[i] << "\n";
	}

	// fill() puts same value in all elements //
	array<int, 5>array4;
	array4.fill(10);
	for (int i = 0; i < array4.size(); i++) {
		cout << "array4[" << i << "] : " << array4[i] << "\n";
	}

	// swap() switches content between arrays //
	array3.swap(array4);
	cout << "Array1 : ";
	for (int element : array3)
		cout << element << " ";
	cout << endl;

	cout << "Array4 : ";
	for (int element : array4)
		cout << element << " ";
	cout << endl;

	// empty() tells if array is empty or not //
	if (array3.empty()) {
		cout << "array3 is empty\n";
	}
	else
	{
		cout << "array3 is not empty\n";
	}

	// example with array of size 0 //
	array <int, 0> array5;
	if (array5.empty()) {
		cout << "array5 is empty\n";
	}
	else
	{
		cout << "array5 is not empty\n";
	}

	// data() gives raw pointer to array //
	int* ptr = array3.data();
	*(ptr + 2) = 20;  // change index 2
	ptr[3] = 30;      // change index 3

	cout << "Array1 : ";
	for (int element : array3)
		cout << element << " ";
	cout << endl;

	// use function to print //
	print_array(array3);

	// using iterator begin() and end() //
	cout << "Array (ip) : ";
	for (array<int, 5>::iterator ar = array3.begin(); ar != array3.end(); ar++) {
		cout << *ar << " ";
	}
	cout << "\n";

	// using auto with iterators //
	cout << "Array (ip) : ";
	for (auto ar = array3.begin(); ar != array3.end(); ar++) {
		cout << *ar << " ";
	}
	cout << "\n";
	
	// using reverse iterators rbegin() and rend() //
	cout << "Array (ip) : ";
	for (auto ar = array3.rbegin(); ar != array3.rend(); ar++) {
		cout << *ar << " ";
	}
	cout << "\n";

	// another way with rbegin/rend //
	cout << "Array (ip) : ";
	for (auto ar = rbegin(array3); ar != rend(array3); ar++) {
		cout << *ar << " ";
	}
	cout << "\n";

	// at() throws exception if index is out of range //
	array<int,5>array6 = { 1,2,3,4,5 };

	try {
		array6.at(5);
	}
	catch (const out_of_range& orr) {
		cout << "ERROR 404 " << orr.what() << "\n";
	}

	return 0;
}
