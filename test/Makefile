

hello: test.cpp
	echo Hello $(what)

what := World


test: test.cpp
	g++ $(CXX_FLAG) test.cpp -o test.exe
	test.exe

CXX_FLAG := -std=c++11