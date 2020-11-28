ANALYSIS = intra-mono-solvertest
FILE = test.cpp
TARGET = $(FILE:.cpp=.ll)
CLANGPLUS = clang++

run: $(TARGET)
	phasar-llvm -D $(ANALYSIS) -m $(TARGET)

$(TARGET): $(FILE)
	$(CLANGPLUS) -S -emit-llvm $< -o $@
