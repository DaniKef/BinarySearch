# BinarySearch
c++

int binary(int* mas, int n, int value, int l, int r) {
	double start1 = clock();
	int s = (l + r) / 2;
	if (l == r) {
		if (value == mas[s]) {
			cout << "Index= " << s << endl;
			return 0;
		}
		else {
			cout << "The value wasn't found" << endl;
			return 0;
		}
	}
	if (mas[s] == value) {
		cout << "Index= " << s << endl;
		double finish1 = clock();
		return 0;
	}
	else if (value < mas[s])
		binary(mas, n, value, l, s - 1);
	else if(value>mas[s])
		binary(mas, n, value, s+1, r);
}
