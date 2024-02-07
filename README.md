[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

[![Github Actions][github-actions-shield]][github-actions]
![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

# WARNING! NOT READY FOR PRODUCTION USE

# Linux Storage Benchmarking Script for Home Assistant Operating System (Customized version of Alpine Linux)

<h2>Overview</h2>
Storage benchmarking script featuring a storage benchmark with a heavy emphasis on random read/write performance (essential for OS / application).  This is far more accurate of a representation of actual performance than simply simulating writing a large file.<br>
<br>
Anonymously uploads your score to pibenchmarks.com for the purposes of making real, meaningful performance comparisons between the different storage devices themselves as well as the platforms they are being used on (PC vs Raspberry Pi vs cloud storage vs others).<br>
<br>
You can optionally supply a username which is used as a sort of tracking tag where you can easily see all benchmarks you've ever taken across all devices!<br>

<h2>View Results</h2>

View the full results at: https://pibenchmarks.com/<br>

<h2>Running the Benchmark</h2>
To run the benchmark type/paste:<br>
<pre>sudo curl https://raw.githubusercontent.com/toddlahman/rPiBenchmarks/master/Storage.sh | sudo bash</pre><br>
If you want to choose which drive to test you can also use:<br>
<pre>
wget https://raw.githubusercontent.com/toddlahman/rPiBenchmarks/master/Storage.sh<br>
chmod +x Storage.sh<br>
sudo ./Storage.sh /path/to/storage</pre><br>

<h2>Removing Installed Packages</h2>
Most of the packages the script installs are core system packages most of which should already be present.  There are a couple benchmarking-only related ones that should be safe to remove if you want an absolute minimalist system.<br>
<br>
If you want to remove the packages the script installed afterward you may do:<br>
<br>
sudo apt remove iozone3 fio<br>
<br>
These are iozone and fio which are both benchmarking utilities and should be safe to use unless you have something else installed that relies on them as a dependency (probably not likely but possible so make sure before removing packages).  

<h2>Changelog</h2>

<h3>2/6/2024</h3>
<ul>
  <li>Initial release</li>
</ul>