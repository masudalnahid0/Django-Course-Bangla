# জ্যাঙ্গো লিংক শর্টেনার

কোন লিংক শর্টেনার এ আমরা যখন লং ইউ আর এল পেস্ট করি তখন এর বিপরীতে ওই ডোমেইন নেমের বিপরীতে একটা শর্ট ইউ আর এল তৈরী হয় । শর্ট ইউ আর এল মুলত এমন sitename/(রেন্ডম কিছু ডিজিট ও লেটার )। তাই লিংক শর্টেনার তৈরী করার জন্য আমাদের প্রথমেই যেটা একটা ফাংশন ডেভেলপ করতে হবে যেটা এইভাবে রেন্ডম স্ট্রিং জেনারেট করবে । এই টিউটোরিয়ালে মুলত সেই ফাংশন্টাই দেখানো হয়েছে । 

---
এরজন্য আমরা পাইথনের দুইটা মডিউল ব্যবহার করব । এই দুইটা হচ্ছে string ও random । ডিফল্টভাবেই এই দুইটা মডিউল ইন্সটল করাই থাকে। তাই আমাদের শুধু ইম্পোর্ট করে নিলেই হবে ।

```code
import string 
import random 
```

এখানে লজিক হচ্ছে স্ট্রিং মডিউল থেকে আমরা ASCII_LETTERS ও ডিজিট গুলা নিয়ে সেখান থেকে রেন্ডমলি আমরা ৪/৫ টি সিলেক্ট করব । 

ASCII_LETTERS এর জন্য আমরা যদি string.ascii_letters কল করলেই a-z ও A-Z সব লেটার দেখাবে । আর string.digit এ কল করলেই আমাদের ০১২৩৪৫৬৭৮৯ ডিজিট নিয়ে নিবে । দুইটা স্ট্রিং কে যোগ করব । এরপর random.sample এর মাধ্যমে আমরা ৪/৫ লেটার চয়েস করব । তবে সেটা আসবে লিস্ট আকারে । লিস্টকে .join() এর মাধ্যমে আমরা স্ট্রিং এ কনভার্ট করে নিব । পুরা কোড হবে নিচের মত 

```code
import random
import string


def sample_generator():
    letters = string.ascii_letters
    digits = string.digits
    character = letters+digits
    sample_character = ''.join(random.sample(character, 4))
    return sample_character
```

আলাদা ফাইল হিসাবেও এখানে সেভ করা হয়েছে । 
---



