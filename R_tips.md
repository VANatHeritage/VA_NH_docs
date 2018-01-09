## R setup, tips

#### Maintaining packages

If you want to maintain a library separate from the base location library that R installs, you can specify a folder to use. This will make upgrading R and your packages easier. To do so:

1. create a new folder to hold your R packages (e.g., `C:/my_r_packages`)

2. Open R, and run the command `.libPaths()`: this will tell you the current places R looks for packages. Copy the path(s) that it returns.

3. Now open the `C:/Program Files/R/[R-CURRENT-VERSION]/etc/Rprofile.site` file with a text editor (open with admin privileges, as you'll need them to edit the file). This specifies settings that run every time R opens. You can add a line at the beginning to specify the R package library folders, e.g.:

   ```
   .libPaths(c("C:/my_r_packages","C:/Users/user/Documents/R/win-library/3.4","C:/Program Files/R/R-3.4.1/library"))
   ```

   - Note that the new folder you created is listed first, before the two that were listed in the `.libPaths()` call from step 2.


#### Other settings for `Rprofile.site`

To stop R from automatically converting character strings to factors when you load data from an external file (the default):

```
options(stringsAsFactors = FALSE)
```

#### Upgrading R

New releases come out every couple months. The recommended method for updating your version of R is:

1. Uninstall the previous version (using the Windows uninstall programs tool)
2. Download and install the new R version.
3. Run through steps 2-3 in the **Maintaining packages** section (since `Rprofile.site` is a new file with the new install)
4. In R, run the command: `update.packages(ask = FALSE, checkBuilt = TRUE)`.
   - this will update all your packages, re-installing those built on a previous version of R (this should help minimize any compatibility issues)







