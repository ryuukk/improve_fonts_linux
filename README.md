# Guide to have beautiful fonts on linux (Arch - Manjaro)

- Packages
  - adobe-source-code-pro-fonts
  - adobe-source-sans-fonts
  - adobe-source-han-sans-cn-fonts
  - adobe-source-han-sans-kr-fonts
  - adobe-source-han-sans-jp-fonts
  - cantarell-fonts
  - noto-fonts
  - noto-fonts-emoji
  - ttf-ubuntu-font-family
  - ttf-anonymous-pro
  - ttf-bitstream-vera
  - ttf-cascadia-code
  - ttf-dejavu
  - ttf-liberation

- AUR
  - freetype2-ultimate5
  - fontconfig-ubuntu
  - ttf-segoe-ui-variable


Once installed:

1. ``ln -s /etc/fonts/conf.avail/11-lcdfilter-default.conf /etc/fonts/conf.d/``


2.  - Settings -> Appearence -> Fonts
    - Default Font: Ubuntu Regular 11px
    - Default Monospace Font: Cascadia Mono Regular 11px
    - Rendering -> Enable anti-aliasing: true
    - Hinting: Slight
    - Sub-pixelorder: RGB
    - ( if you are on gnome: ``gsettings set org.gnome.settings-daemon.plugins.xsettings antialiasing rgba`` )
  
 
3. - Create the local fonts.conf file (~/.config/fontconfig/fonts.conf)
   - Paste content from below
   - ``fc-cache -f``
   - reboot

```xml
<?xml version="1.0" encoding="UTF-8"?>
<fontconfig>
   <alias>
      <family>sans-serif</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>Roboto</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>Helvetica</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>Ginto</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>Whitney</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>Inter</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>ui-monospace</family>
      <prefer>
         <family>Cascadia Mono</family>
         <family>Cascadia Code</family>
         <family>Ubuntu Mono</family>
         <family>Bitstream Vera Sans Mono</family>
         <family>Inconsolata</family>
         <family>Andale Mono</family>
         <family>Courier New</family>
         <family>Cumberland AMT</family>
         <family>Luxi Mono</family>
         <family>Nimbus Mono L</family>
         <family>Nimbus Mono</family>
         <family>Nimbus Mono PS</family>
         <family>Courier</family>
      </prefer>
   </alias>
   <alias>
      <family>monospace</family>
      <prefer>
         <family>Cascadia Mono</family>
         <family>Cascadia Code</family>
         <family>Ubuntu Mono</family>
         <family>Bitstream Vera Sans Mono</family>
         <family>Inconsolata</family>
         <family>Andale Mono</family>
         <family>Courier New</family>
         <family>Cumberland AMT</family>
         <family>Luxi Mono</family>
         <family>Nimbus Mono L</family>
         <family>Nimbus Mono</family>
         <family>Nimbus Mono PS</family>
         <family>Courier</family>
      </prefer>
   </alias>
   <alias>
      <family>-apple-system</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
   <alias>
      <family>BlinkMacSystemFont</family>
      <prefer>
         <family>Ubuntu</family>
      </prefer>
   </alias>
</fontconfig>
``` 
