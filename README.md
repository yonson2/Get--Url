## Get::Url - provide path. get url.
### A Perl implementation of [uams](https://github.com/uams) [geturl](https://github.com/uams/geturl), a CLI tool to get a public link for any file. 

#### Usage
    get-url file1 file2

<img src="https://raw.github.com/psychotropic/get--url/master/upload.png">


#### Dependencies
install using cpan or [cpanm](https://github.com/miyagawa/cpanminus/) (some of them should be already bundled with perl)

    LWP::Protocol::https File::HomeDir File::Slurp File::Basename Cwd DBM::Deep URI::Encode LWP::UserAgent Digest::SHA1 utf8
#### Installation

    sudo curl https://raw.github.com/psychotropic/get--url/master/get-url -o /usr/bin/get-url;
    sudo chmod +x /usr/bin/get-url

Enable Clipboard Access (Only necessary on Linux)

    sudo apt-get install xclip

#### Notes
it should be cross-platform. (Only tested on linux)

If caching is enabled a SHA1 of your file and it's correspondant URL will be stored on a database to be retrieved later and avoid having to reupload the same data.

The config file generated remains compatible with [geturl](https://github.com/uams/geturl) in case you want to go back but you should delete your `.geturl` file if you want to switch to Get::Url.