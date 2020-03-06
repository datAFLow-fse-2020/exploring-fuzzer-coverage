# Exploring Fuzzer Coverage: Control Flow versus Data Flow

This repo contains supplementary material for the ESEC/FSE 2020 submission:
"Exploring Fuzzer Coverage: Control Flow versus Data Flow" (submission #93).

It is structured as follows:

* **RQ1** [Bug discovery](bugs.md)
* **RQ2** [Coverage plots](coverage_plots.md)
* **RQ3** [Performance overhead](performance_overhead.md)

The results describe the following targets:

| Program | Version | File type          | Driver                       |
|---------|---------|--------------------|------------------------------|
| Bison   | 3.5     | Grammar            | `bison -o /dev/null @@`      |
| c++filt | 2.34    | Text               | `cxxfilt < @@`               |
| JSON-C  | 0.13.1  | JSON               | `tokener_parse_ex_fuzzer @@` |
| LibTIFF | 4.1.0   | TIFF               | `tiff2pdf -o /dev/null @@`   |
| Lua     | 5.3.5   | Lua                | `lua @@`                     |
| mJS     | 2.17.0  | JavaScript         | `mjs -f @@`                  |
| NASM    | 2.14.02 | Assembly           | `nasm -o /dev/null @@`       |
| PCRE2   | 10.34   | Regular expression | `pcre2fuzzcheck @@`          |
| Poppler | 0.84.0  | PDF                | `pdftotext /dev/null @@`     |
| readelf | 2.34    | ELF                | readelf --all @@             |
