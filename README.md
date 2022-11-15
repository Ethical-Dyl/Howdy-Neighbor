# Howdy-Neighbor
A writeup of the TryHackMe CTF challenge 'Neighbour'

# Initial Enumeration
My nmap scans had shown two active ports open:
<img width="448" alt="image" src="https://user-images.githubusercontent.com/66540055/202032988-9d8fe3ff-e6e2-46ab-be96-a4e357dbecc1.png">

# Web Enumeration
Crawling the main page I am hinted to use the guest account, and strangely enough to view the page source:
<img width="501" alt="image" src="https://user-images.githubusercontent.com/66540055/202033439-fead687e-42c8-4635-9b9e-77ad82e2c8b1.png">

Using the credentials provided I am now logged in as guest. From the URL I will attempt to view the admin profile by changing the paramaters from guest to admin:
<img width="951" alt="image" src="https://user-images.githubusercontent.com/66540055/202033930-afed6647-4366-46bf-abed-8412cd483258.png">

<img width="377" alt="image" src="https://user-images.githubusercontent.com/66540055/202034071-b386577c-377a-4b8a-b0b4-249fd8eaebcd.png">

Awesome! That worked, the flag is now available for turn-in:
<img width="958" alt="image" src="https://user-images.githubusercontent.com/66540055/202034182-5cb05532-8e2c-46a8-9367-f3c93c42b943.png">

# Final Thoughts

This is a simple to exploit and fun way to showcase how IDOR vulnerabilities can be harmful in the wild, imagine if your bank did not have implementations in place to safeguard hackers' and other users from viewing profiles that are not their own. Thankfully most companies today have protections from the simpler forms of these attack vectors in the attempts to keep our private data safe.
