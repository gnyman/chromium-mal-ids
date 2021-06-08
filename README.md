# chrome-mal-ids

This is a fork from https://github.com/mallorybowes/chrome-mal-ids, might get merged back at some point.

A list of known "bad" Chromium extensions and a helper script to look trough your computer to see if you have them, only works with Ubunut Brave (snap), Linux Chrome, OS X Chrome and OS X Brave.

If you don't want to download and run the script, you can just run the following command in your terminal. This should work on any bash, remember to fix the path if you're not checking Chrome/Brave on OS X.

`join <(curl -s https://raw.githubusercontent.com/gnyman/chromium-mal-ids/master/current-list.csv | sort) <( basename ${HOME}/Library/Application\ Support/{Google/Chrome,BraveSoftware/Brave-Browser-Beta}/Default/Extensions/* | sort ) | xargs -I% echo "Found bad extension https://chrome.google.com/webstore/detail/%"`

If it finds anything it will output
```
Found bad extension https://chrome.google.com/webstore/detail/[ID]
```
if it finds nothing, it won't output anything.

*Sources of the compromised list:* 

#### May 2, 2021 
Krebs on Security find suspicious extensions by cross referencing fake reviews. https://krebsonsecurity.com/2021/05/using-fake-reviews-to-find-dangerous-extensions/

#### May 18, 2021
Don't download this Microsoft Authenticator extension for Chrome: it is fake https://www.ghacks.net/2021/05/18/dont-download-this-microsoft-authenticator-extension-for-chrome-it-is-fake/#snhb-snhb_ghacks_bottom-0

#### Feb 5, 2021
Malicious extension abuses Chrome sync to steal users’ data https://www.bleepingcomputer.com/news/security/malicious-extension-abuses-chrome-sync-to-steal-users-data/

Since this one seems to center around syncing, I'm just going to add to the list immediately and watch for any qualifying reasons to remove it.  Since it wasn't in the Chrome Store, I was left with looking at the graphic in the article to get the extension ID.  

```
fmfjhicbjecfchfmpelfnifijeigelme
```

#### Feb 4, 2021
Google just booted The Great Suspender off the Chrome Web Store for being malware https://www.xda-developers.com/google-chrome-the-great-suspender-malware/

Looks like it's official now so moved the Great Suspender to the malicious column...

#### Feb 3, 2021
Backdoored Browser Extensions Hid Malicious Traffic in Analytics Requests https://decoded.avast.io/janvojtesek/backdoored-browser-extensions-hid-malicious-traffic-in-analytics-requests/

Most of these extensions were already in the current list except for the following three that were added:

```
akdbogfpgohikflhccclloneidjkogog
lgjogljbnbfjcaigalbhiagkboajmkkj
aemaecahdckfllfldhgimjhdgiaahean
```

#### Jan 15, 2021
Facebook sues makers of malicious Chrome extensions for scraping data https://www.bleepingcomputer.com/news/security/facebook-sues-makers-of-malicious-chrome-extensions-for-scraping-data/

```
dppilebghcniomddkpphiminideiajff
ojmbbkdflpfjdceflikpkbbmmbfagglg
chmaijbnjdnkjknoigffoohjhpejjppd
jhcfnojahmdghhebdaoijngclknfkbjn
```

#### Jan 5, 2021
Ditch 'The Great Suspender' Before It Becomes a Security Risk  https://lifehacker.com/ditch-the-great-suspender-before-it-becomes-a-security-1845989664

Ugh.  This one hit close to home and on the plus side, I may have finally installed a malicious extension. :-/  I haven't seen an article that *confirms* it's suspicious yet so I'm holding off putting in the list until further confirmation.  (Please let me know if there's confirmation of malicious behavior but I hate there's a possibility that "The Great Suspender" may now be malicious.)

Extension ID:
```
klbibkeccnjlkjkiokjodocebajanakg
```

#### Dec 26, 2020
Dangerous Chrome extensions https://www.kaspersky.com/blog/chrome-plugins-alert/38242/ 

I'm not going to officially add these extensions to the overall list just yet since I've only been able to find one source on a Russian blog site. (https://habr.com/en/company/yandex/blog/534586/) Anyway, I'll publish the list of extensions listed in the blog post below and will wait on additional confirmation before adding to the overall archive list.

Extension IDs:
```
acdfdofofabmipgcolilkfhnpoclgpdd
oobppndjaabcidladjeehddkgkccfcpn
aonedlchkbicmhepimiahfalheedjgbh
aoeacblfmdamdejeiaepojbhohhkmkjh
eoeoincjhpflnpdaiemgbboknhkblome
onbkopaoemachfglhlpomhbpofepfpom
inlgdellfblpplcogjfedlhjnpgafnia
ejfajpmpabphhkcacijnhggimhelopfg
pgjndpcilbcanlnhhjmhjalilcmoicjc
napifgkjbjeodgmfjmgncljmnmdefpbf
glgemekgfjppocilabhlcbngobillcgf
klmjcelobglnhnbfpmlbgnoeippfhhil
ldbfffpdfgghehkkckifnjhoncdgjkib
mbacbcfdfaapbcnlnbmciiaakomhkbkb
mdnmhbnbebabimcjggckeoibchhckemm
lfedlgnabjompjngkpddclhgcmeklana
mdpljndcmbeikfnlflcggaipgnhiedbl
npdpplbicnmpoigidfdjadamgfkilaak
ibehiiilehaakkhkigckfjfknboalpbe
lalpacfpfnobgdkbbpggecolckiffhoi
hdbipekpdpggjaipompnomhccfemaljm
gfjocjagfinihkkaahliainflifnlnfc
ickfamnaffmfjgecbbnhecdnmjknblic
bmcnncbmipphlkdmgfbipbanmmfdamkd
miejmllodobdobgjbeonandkjhnhpjbn
```

#### Dec 19, 2020
Three million users installed 28 malicious Chrome or Edge extensions https://www.zdnet.com/article/three-million-users-installed-28-malicious-chrome-or-edge-extensions/ (Shouts to [nycnewman](https://github.com/nycnewman) for messaging me about the breaking story!  Thank you!)

Because it took me awhile to find the exact extension IDs for this, I decided to post the IDs here for a bit to help other researchers get an easy text listing of the IoCs.

Extension IDs:
```
mdpgppkombninhkfhaggckdmencplhmg
fgaapohcdolaiaijobecfleiohcfhdfb
iibnodnghffmdcebaglfgnfkgemcbchf
olkpikmlhoaojbbmmpejnimiglejmboe
bhfoemlllidnfefgkeaeocnageepbael
nilbfjdbacfdodpbdondbbkmoigehodg
eikbfklcjampfnmclhjeifbmfkpkfpbn
pfnmibjifkhhblmdmaocfohebdpfppkf
cgpbghdbejagejmciefmekcklikpoeel
klejifgmmnkgejbhgmpgajemhlnijlib
ceoldlgkhdbnnmojajjgfapagjccblib
mnafnfdagggclnaggnjajohakfbppaih
oknpgmaeedlbdichgaghebhiknmghffa
pcaaejaejpolbbchlmbdjfiggojefllp
lmcajpniijhhhpcnhleibgiehhicjlnk
lnocaphbapmclliacmbbggnfnjojbjgf
bhcpgfhiobcpokfpdahijhnipenkplji
dambkkeeabmnhelekdekfmabnckghdih
dgjmdlifhbljhmgkjbojeejmeeplapej
emechknidkghbpiodihlodkhnljplpjm
hajlccgbgjdcjaommiffaphjdndpjcio
dljdbmkffjijepjnkonndbdiakjfdcic
cjmpdadldchjmljhkigoeejegmghaabp
jlkfgpiicpnlbmmmpkpdjkkdolgomhmb
njdkgjbjmdceaibhngelkkloceihelle
phoehhafolaebdpimmbmlofmeibdkckp
pccfaccnfkjmdlkollpiaialndbieibj
fbhbpnjkpcdmcgcpfilooccjgemlkinn
```

#### Oct 28, 2020
Just fyi, the extensions used in the Kimsuky / Hidden Cobra [CISA alert AA20-302A](https://us-cert.cisa.gov/ncas/alerts/aa20-301a) are already listed in current extension list.

#### Oct 21, 2020
Adblockers installed 300,000 times are malicious and should be removed now  https://arstechnica.com/information-technology/2020/10/popular-chromium-ad-blockers-caught-stealing-user-data-and-accessing-accounts/

#### Oct 2, 2020
Facebook sues two Chrome extension makers for scraping user data (2 extensions added) https://www.zdnet.com/article/facebook-sues-two-chrome-extension-makers-for-scraping-user-data/

#### Aug 4, 2020
Cluster of 295 Chrome extensions caught hijacking Google and Bing search results  https://www.zdnet.com/article/cluster-of-295-chrome-extensions-caught-hijacking-google-and-bing-search-results/

#### Jun 19, 2020
Found a extension that contains malware (2 extensions added) https://www.reddit.com/r/chrome/comments/hbpi7z/found_a_extension_that_contains_malware/

#### Jun 18, 2020
Google removes 106 Chrome extensions for collecting sensitive user data https://www.zdnet.com/article/google-removes-106-chrome-extensions-for-collecting-sensitive-user-data/ https://awakesecurity.com/wp-content/uploads/2020/06/GalComm-Malicious-Chrome-Extensions-Appendix-B.txt

#### Apr 16, 2020
49 malicious Chrome extensions caught pickpocketing crypto wallets  https://medium.com/mycrypto/discovering-fake-browser-extensions-that-target-users-of-ledger-trezor-mew-metamask-and-more-e281a2b80ff9

#### Feb 13, 2020
Security Researchers Partner With Chrome To Take Down Browser Extension Fraud Network Affecting Millions of Users https://duo.com/labs/research/crxcavator-malvertising-2020

#### Jan 1, 2020
Chrome extension caught stealing crypto-wallet private keys https://www.zdnet.com/article/chrome-extension-caught-stealing-crypto-wallet-private-keys/

#### Jul 22, 2019
Malicious browser extensions are stealing personal information https://www.salon.com/2019/07/22/malicious-browser-extensions-are-stealing-personal-information/  https://dataspii.com/

#### May 10, 2018
Nigelthorn Malware Abuses Chrome Extensions to Cryptomine and Steal Data https://blog.radware.com/security/2018/05/nigelthorn-malware-abuses-chrome-extensions/

#### Jan 18, 2018
Malicious Chrome Extensions Enable Criminals to Impact Half a Million Users and Global Businesses https://atr-blog.gigamon.com/2018/01/18/malicious-chrome-extensions-enable-criminals-to-impact-half-a-million-users-and-global-businesses/

#### Aug 16, 2017
Bank-fraud malware not detected by any AV hosted in Chrome Web Store. Twice https://arstechnica.com/information-technology/2017/08/bank-fraud-malware-not-detected-by-any-av-hosted-in-chrome-web-store-twice/

 
