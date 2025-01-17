# encode / decode
## Abstract
`encode_decode.hpp` contains functions for encoding and decoding operations.
`encode_decode.hpp` はエンコード・デコードにまつわる関数を収録します．

## Header file
```cpp
namespace sstd{
    std::string base64_encode(const uchar* str, size_t strLen);
    std::string base64_encode(const uchar* str);
    std::string base64_encode(const std::string& str);

    std::string base64_decode(const uchar* str, size_t strLen); // when it was an error, 0 size std::string is returned.
    std::string base64_decode(const uchar* str);                // when it was an error, 0 size std::string is returned.
    std::string base64_decode(const std::string& str);          // when it was an error, 0 size std::string is returned.
    void print_base64_decode_table(); // for developers

    extern const char bin2str_table[256][3];
    std::string url_encode(const char* str, size_t strLen);
    std::string url_encode(const char* str);
    std::string url_encode(std::string& str);
    std::string url_encode_type2(const char* str, size_t strLen); // for developers
    void url_encode_compare_speed(); // for developers

    std::string url_decode(const char* str, size_t strLen); // when it was an error, 0 size std::string is returned.
    std::string url_decode(const char* str);                // when it was an error, 0 size std::string is returned.
    std::string url_decode(std::string& str);               // when it was an error, 0 size std::string is returned.
    void print_url_decode_table(); // for developers

//  std::u16string utf8_to_utf16(const std::string& str);
//  std::string utf16_to_utf8(const std::u16string& str);
    // utf functions are not checked yet.
    std::u32string utf16_to_utf32(const std::u16string& str);
    std::u16string utf32_to_utf16(const std::u32string& str);
    std::   string utf32_to_utf8 (const std::u32string& str);
    std::u32string  utf8_to_utf32(const std::   string& str);
    std::u16string  utf8_to_utf16(const std::   string& str);
    std::   string utf16_to_utf8 (const std::u16string& str);

    extern const uchar str2bin_table[256];
    std::string    unicodeEscape_encode(const std::u16string& str);
    std::u16string unicodeEscape_decode(const char* str, size_t strLen);
    std::u16string unicodeEscape_decode(const char* str);
    std::u16string unicodeEscape_decode(const std::string& str);
    std::u16string unicodeEscape_decode_type2(const char* str, size_t strLen); // for developers
    void unicodeEscape_compare_speed(); // for developers
    void print_unicodeEscape_decode_table();
};
```

## Usage
- <u>**main.cpp**</u>
```cpp
#mdEx: cpp example (in)
#include <sstd/sstd.hpp>

int main(){
    return 0;
}
```
- <u>**Execution result**</u>
```
#mdEx: cpp example (out)
```

## Implementation
- Source: [sstd/src/encode_decode.cpp](https://github.com/admiswalker/SubStandardLibrary-SSTD-/blob/master/sstd/src/encode_decode.cpp)
- Header: [sstd/src/encode_decode.hpp](https://github.com/admiswalker/SubStandardLibrary-SSTD-/blob/master/sstd/src/encode_decode.hpp)
- Test: [test/encode_decode.hpp](https://github.com/admiswalker/SubStandardLibrary-SSTD-/blob/master/test/encode_decode.hpp)
  (Not implemented yet)

