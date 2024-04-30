# Dependencies Analysis for Golang projects

# The workflow use:

 - actions/checkout@v4
 - actions/setup-go@v5
 - actions/upload-artifact@v4

## Before to copy content to .txt file

    go mod tidy
   run for organize and clean go.mod and go.sum file

## Generate report

    echo -e "Content go.mod\n" > dependenciesAnalysis.txt
    cat go.mod >> dependenciesAnalysis.txt
    echo -e "\nContent go.sum\n" >> dependenciesAnalysis.txt
    cat go.sum >> dependenciesAnalysis.txt

## Upload report

    with:
      name: dependencies-report
      path: ./dependenciesAnalysis.txt
