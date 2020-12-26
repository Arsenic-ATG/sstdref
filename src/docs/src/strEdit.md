# strEdit
## Abstract
strEdit.hpp / strEdit.cpp は，文字列を編集するための関数を収録している．

## Header file
```c++
namespace sstd{
    std::vector<uint8>       readAll_bin(const char*        pReadFile); // read all of the file as a binary
    std::vector<uint8>       readAll_bin(const std::string&  readFile); // read all of the file as a binary
    
    bool                     writeAll_bin(const char*        pWritePath, std::vector<uint8>& rhs);
    bool                     writeAll_bin(const std::string&  writePath, std::vector<uint8>& rhs);
    
    std::string              readAll(const char*        pReadFile); // readAll_str()
    std::string              readAll(const std::string&  readFile); // readAll_str()
    std::string              readAll_withoutBOM(const char*        pReadFile);
    std::string              readAll_withoutBOM(const std::string&  readFile);
    std::vector<std::string> splitByLine(const std::string& str);
    
    std::vector<std::string> split(const char*        str, const char X);
    std::vector<std::string> split(const std::string& str, const char X);
    
    // remove space or tab.
    std::string              lstrip   (const        char* str); // removing head spaces
    std::string              lstrip   (const std::string& str); // removing head spaces
    void                     lstrip_ow(      std::string& str); // removing head spaces. ow: overwrite
    std::string              rstrip   (const        char* str); // removing tail spaces
    std::string              rstrip   (const std::string& str); // removing tail spaces
    void                     rstrip_ow(      std::string& str); // removing tail spaces. ow: overwrite
    std::string               strip   (const        char* str); // removing head and tail tab and spaces
    std::string               strip   (const std::string& str); // removing head and tail tab and spaces
    void                      strip_ow(      std::string& str); // removing head and tail tab and spaces. ow: overwrite
    std::vector<std::string>  strip   (const std::vector<std::string>& vec); // -> strip(str) // removing head and tail spaces
    
    bool strcmp(const char*        str1, const char*        str2);
    bool strcmp(const char*        str1, const std::string& str2);
    bool strcmp(const std::string& str1, const char*        str2);
    bool strcmp(const std::string& str1, const std::string& str2);
    
    bool strIn(const char*        lhs, const char*        rhs); // is lhs in rhs ? (is rhs include lhs ?)
    bool strIn(const char*        lhs, const std::string& rhs);
    bool strIn(const std::string& lhs, const char*        rhs);
    bool strIn(const std::string& lhs, const std::string& rhs);
}
```

## Usage

## Others
- Implementation: [sstd/src/vector/strEdit.hpp](https://github.com/admiswalker/SubStandardLibrary-SSTD-/blob/master/sstd/src/strEdit.hpp)
- Test code: [test/strEdit.hpp](https://github.com/admiswalker/SubStandardLibrary-SSTD-/blob/master/test/strEdit.hpp)
