BUILD_DIR = host
SOURCES=main.cpp part1.cpp part2.cpp
OBJECTS=$(addprefix ${BUILD_DIR}/, ${SOURCES:.cpp=.o})
EXECUTABLE=main
CXX=g++

all: ${OBJECTS}
	${CXX} -o ${BUILD_DIR}/${EXECUTABLE} ${OBJECTS}

${BUILD_DIR}/%.o: %.cpp ${BUILD_DIR}
	${CXX} -c -o $@ $<

clean: 
	@rm -rf ${BUILD_DIR}

help:
	@echo "Targets:"
	@echo "  all"
	@echo "  clean"
	@echo "  help"
	@echo ""
	@echo "Vars:"
	@echo "  CXX"
	@echo "  EXECUTABLE"
	@echo "" 

${BUILD_DIR}:
	mkdir -p ${BUILD_DIR}
