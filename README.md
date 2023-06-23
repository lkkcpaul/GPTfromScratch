# GPTfromScratch
This is my exercise for building GPT from scratch to better understand self attention and transformer.
I mainly followed this tutorial https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy.
This is not a fine-tuning of a pretrained model. 

I first trained on the Chinese text 論語 ("Analects of Confucius") and then on 紅樓夢 ("Dream of Red Mansion"), 
the reason being Chinese tokenization is easier and there's less Chinese examples out there. 

This runs on the GPU (NVidia GeForce RTX 2060 ) on my laptop. 
The output follows the style of the input text and makes some sensiblesentences here and there. 

An example text generated using 論語:
---------------------------------------------------
子曰君不臧以禮乎揖讓為謀

子張問弟之出曰君子之


子不信好禮後食如子對曰恭出曰報德

子張我者利子曰先進第十子曰求也



子曰居之下治信行必趨

子貢曰先人吾道不倦何何謂之曰聽乎改於


An example text generated using 紅樓夢
---------------------------------------------------
宝玉如了好，只怕完了。宝钗看了，只见莺儿两个丫头三个嵌了这花帖子似秋，见他猛然见什么话，只见紫鹃呆雁起来，只见香菱并诧异，方乱叫了一句：“二哥哥相找，多少向么骄窸吕吕蠢物，大哥儿说了。”说着个声竟

A 5000 character example of text generation using 紅樓夢 is in "generated.txt". 
As you can see, the certainly looks like 紅樓夢 in style and some sentences almost make sense. 
All the codes are in the ChineseGPT notebook. Run it to build and train your own model.
"hongloumeng.txt" and "lunyu.txt" are the text files used for training.
"model_hlm.pt" contains the best trained model, with validation loss = 3.9. 
You can download that pre-trained model in the release.
To load the model and generate your own text, simply use the torch.load function (as shown in the notebook)

Feel free to use my code and I'm open to suggestions. 


