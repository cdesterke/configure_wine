# configure_wine
configuration de wine avec R and Rtools

'''
sudo apt install wine
wine R-4.5.2-win.exe
'''

## ~/.wine/drive_c/Program Files/R/R-4.5.2/


wine rtools45-6691-6492.exe


## ~/.wine/drive_c/rtools45/


## config path
### Dans ~/.wine/drive_c/Program Files/R/R-4.5.2/etc/Rprofile.site, ajoute :

Sys.setenv(PATH = paste("C:/rtools45/usr/bin;C:/rtools45/mingw64/bin;", Sys.getenv("PATH"), sep=""))


## Place ton .tar.gz dans un dossier accessible par Wine,
wine "C:/Program Files/R/R-4.5.2/bin/R.exe" CMD INSTALL --build chi2residuals_0.1.1.tar.gz

## R comandline dans terminal
wine "C:/Program Files/R/R-4.5.2/bin/R.exe"

## wine R-GUI sous ubuntu
wine "C:/Program Files/R/R-4.5.2/bin/x64/Rgui.exe"

## R

pkgbuild::find_rtools()
Sys.getenv("PATH")
