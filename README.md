# Obfuscated-String-Builder
Obfuscated String Builder C/C++

TryMe - https://jakeloganuk.github.io/root/ObfuscateString/


- [x] Example String - "My Strings Here"
```
unsigned char s[] = 
{

    0xa3, 0xf7, 0xfe, 0xd1, 0xe6, 0xe4, 0xbb, 0xe4, 
    0xb9, 0xf5, 0xfe, 0xca, 0xeb, 0xe4, 0xe7, 0xd2
};

for (unsigned int m = 0; m < sizeof(s); ++m)
{
    unsigned char c = s[m];
    c += m;
    c ^= 0xe4;
    c += 0x33;
    c = ~c;
    c ^= 0x36;
    c = -c;
    c -= m;
    s[m] = c;
}
cout << s << endl;
```
