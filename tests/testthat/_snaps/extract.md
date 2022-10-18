# informative error message if wrong number of groups

    Code
      (expect_error(extract(df, x, "y", ".")))
    Output
      <error/rlang_error>
      Error in `extract()`:
      ! `regex` should define 1 groups; 0 found.
    Code
      (expect_error(extract(df, x, c("y", "z"), ".")))
    Output
      <error/rlang_error>
      Error in `extract()`:
      ! `regex` should define 2 groups; 0 found.

# informative error if using stringr modifier functions (#693)

    Code
      (expect_error(extract(df, x, "x", regex = regex)))
    Output
      <error/rlang_error>
      Error in `extract()`:
      ! `regex` can't use modifiers from stringr.
