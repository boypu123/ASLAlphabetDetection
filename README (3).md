# ASLSpellingGame

This API is a part of a final project of PACSAR-201005, Introduction to Machine Learning and Neural Networks course. By Group 1. <br>

ASL Alphabet Classification API:
- Lightweight API
- Classifies the gestures of ALPHABETS of ASL.
- Node.js
<br>

## Example Input & Output
Input (Raw Features, as JSON format, 96x96 image, some content is omitted here since the input is too large): <br>
```json
{
	"userInput": "0xb8c1c2, 0xb6c1c0, 0xbfc8c4, 0xbcc6c0, 0xbdc7c4, 0xbbc5bf, 0xb8c2bc, 0xb7c1bc, 0xb4beb8, 0xb1b9b3, 0xaeb6af, 0xa9b1aa, 0xa3ada5, 0xa0a7a0, 0x9ba098, 0x979a92, 0x91958d, 0x8c8f87, 0x858880, 0x82847f, 0x7e7f77, 0x7d7e78, 0x7e7f77, 0x808078, 0x7f827c, 0x7f827c, 0x80837c, 0x81847f, 0x818481, 0x828580, 0x838681, 0x828682, 0x818883, 0x828985, 0x848985, 0x848985, 0x858a86, 0x858a86, 0x868a86, 0x888b87, 0x888b87, 0x868b87, 0x868b87, 0x878b88, 0x878c88, 0x868c88, 0x868c88, 0x878d89, 0x868d89, 0x868d89, 0x868c8a, 0x868b8a, 0x868b8a, 0x868b8a, 0x868b8a, 0x858b89, 0x848b89, 0x848b88, 0x848b89, 0x858a88, 0x858a88, 0x848987, 0x838987, 0x838886, 0x808885, 0x808785, 0x7f8684, 0x7f8581, ..., 0x838a85, 0x828a85, 0x818783, 0x818682, 0x828783, 0x808782, 0x7e8580, 0x7e8480, 0x808581, 0x828783, 0x828783, 0x818682, 0x808783, 0x808682, 0x7f8380, 0x7c847f, 0x7f837f, 0x7d837e, 0x7e827f, 0x7e837f, 0x7c817e, 0x7c817d, 0x7c807a, 0x7b7f77, 0x7b7f78, 0x7b7e78, 0x7a7e78, 0x787d77, 0x777c78, 0x787e77, 0x767c75, 0x757a74, 0x737771, 0x73766f, 0x72756d, 0x71746c"
}
```
Output: <br>
```json
{
	"final": "{\n    \"anomaly\": 0,\n    \"results\": [\n        {\n            \"label\": \"A\",\n            \"value\": 0.968292772769928\n        },\n        {\n            \"label\": \"B\",\n            \"value\": 1.1727054527455039e-7\n        },\n        {\n            \"label\": \"C\",\n            \"value\": 2.5692931115983697e-10\n        },\n        {\n            \"label\": \"D\",\n            \"value\": 0.000026575533411232755\n        },\n        {\n            \"label\": \"E\",\n            \"value\": 0.00167121144477278\n        },\n        {\n            \"label\": \"F\",\n            \"value\": 0.001129426178522408\n        },\n        {\n            \"label\": \"G\",\n            \"value\": 6.303302768628782e-8\n        },\n        {\n            \"label\": \"H\",\n            \"value\": 3.129874315277448e-8\n        },\n        {\n            \"label\": \"I\",\n            \"value\": 0.00017377834592480212\n        },\n        {\n            \"label\": \"J\",\n            \"value\": 0.00007283339073183015\n        },\n        {\n            \"label\": \"K\",\n            \"value\": 6.437015920290889e-10\n        },\n        {\n            \"label\": \"L\",\n            \"value\": 3.132595960408935e-9\n        },\n        {\n            \"label\": \"M\",\n            \"value\": 0.000016232907000812702\n        },\n        {\n            \"label\": \"N\",\n            \"value\": 0.0000019626138509920565\n        },\n        {\n            \"label\": \"Nothing\",\n            \"value\": 1.6734103880367002e-8\n        },\n        {\n            \"label\": \"O\",\n            \"value\": 0.0020514773204922676\n        },\n        {\n            \"label\": \"P\",\n            \"value\": 5.96962337340301e-8\n        },\n        {\n            \"label\": \"Q\",\n            \"value\": 1.5681835829894908e-9\n        },\n        {\n            \"label\": \"R\",\n            \"value\": 3.361695588566249e-9\n        },\n        {\n            \"label\": \"S\",\n            \"value\": 0.02616538479924202\n        },\n        {\n            \"label\": \"Space\",\n            \"value\": 7.161348491990793e-8\n        },\n        {\n            \"label\": \"T\",\n            \"value\": 0.00020734374993480742\n        },\n        {\n            \"label\": \"U\",\n            \"value\": 9.780188214847385e-9\n        },\n        {\n            \"label\": \"V\",\n            \"value\": 4.522873098267155e-8\n        },\n        {\n            \"label\": \"W\",\n            \"value\": 1.431167078180806e-7\n        },\n        {\n            \"label\": \"X\",\n            \"value\": 0.0001310579536948353\n        },\n        {\n            \"label\": \"Y\",\n            \"value\": 0.00005741552740801126\n        },\n        {\n            \"label\": \"Z\",\n            \"value\": 0.000001987476252907072\n        }\n    ]\n}"
}
```
## What is it & Why are we doing it?
The sign languages - the unique languages which help disabled people to survive and to strive are being ignored. <br>
Do you know that sign languages have their language family? Do you know that sign languages are different depending on the country, just like spoken languages? <br>
The project is a game in which the users can practice the basic alphabet gestures of American Sign Language. <br>
Sadly, there are still many sign languages that do not have a lot of publicly available datasets.

## Methodology
We used Edge Impulse, a low code online machine learning platform, to build a machine learning model that can recognize the basic alphabet gestures of American Sign Language. We used MobileNet V2 96x96 0.25 because it has the most outstanding performance, ensuring that the model is not overfitting while maintaining the accuracy. <br>

We exported this model and connects it with Node.js to build a web application: https://github.com/boypu123/ASLSpellingGame/tree/main<br>

For more information, please visit our slideshow: https://1drv.ms/p/s!ArvHrHRaGEvxoZtdbPeyDoEek2oD6Q?e=fyDTrc

## Installation
### Way 1
Download this file and extract it.

### Way 2
Clone this repository using git. <br>
``git clone git@github.com:boypu123/ASLSpellingGame.git``

## Run

First, ``cd backend`` to the backend folder. Then run ``node server.js`` to run the backend server program<br>

## Team Members (In Alphabetical Order)
Guoxiang Ran, Southeast University, China; https://github.com/Squincat <br>
Hongwen Pu, Dulwich College (Singapore), Singapore; https://github.com/boypu123 <br>
Minghua Ying, Southeast University, China; https://github.com/ahuahaha <br>
Raykio (Keyi) Yi, Dulwich College (Suzhou), China; https://github.com/Raykxia


## Acknowledgement

Thanks to Professor Rogers from University of Oxford, who had been teaching us throughout this course. It is a pleasure for me to be his student in this course. You can find his GitHub page here: https://github.com/AlexRogersCS, and you can find more about him here: https://www.cs.ox.ac.uk/people/alex.rogers/.