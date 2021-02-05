# CoreNLP

Stanford CoreNLP on macOS

## Quick Start

- Install [Java](https://www.java.com/zh-TW/download/)

- Install requirements

	***run*** `pip3 install -r requirements.txt`

## Using CoreNLP

- Sample code

	```
	from corenlp import CoreNLP
	model = CoreNLP("zh")
	sent = "研究生命有多长"
	print(model.word_tokenize(sent))
	print(model.pos_tag(sent))
	print(model.ner(sent))
	print(model.parse(sent))
	print(model.dependency_parse(sent))
	```

- Sample output

	```
	['研究', '生命', '有', '多', '长']
	[('研究', 'VV'), ('生命', 'NN'), ('有', 'VE'), ('多', 'AD'), ('长', 'VA')]
	[('研究', 'O'), ('生命', 'O'), ('有', 'O'), ('多', 'O'), ('长', 'O')]
	(ROOT
	  (IP
	    (IP
	      (VP (VV 研究)
	        (NP (NN 生命))))
	    (VP (VE 有)
	      (IP
	        (VP
	          (ADVP (AD 多))
	          (VP (VA 长)))))))
	[('ROOT', 0, 5), ('dep', 5, 1), ('dobj', 1, 2), ('dep', 5, 3), ('advmod', 5, 4)]
	```

## Uninstall [Java](https://www.java.com/zh-TW/download/help/mac_uninstall_java_zh-tw.html)

```
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
sudo rm -fr /Library/PreferencesPanes/JavaControlPanel.prefPane
sudo rm -fr ~/Library/Application\ Support/Java
```
