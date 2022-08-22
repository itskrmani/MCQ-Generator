Models:
	AllenNLP coref spanbert - https://storage.googleapis.com/allennlp-public-models/coref-spanbert-large-2021.03.10.tar.gz

	Bert-WSD - https://entuedu-my.sharepoint.com/personal/boonpeng001_e_ntu_edu_sg/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fboonpeng001%5Fe%5Fntu%5Fedu%5Fsg%2FDocuments%2FBERT%2DWSD%2Fmodel%2Fbert%5Fbase%2Daugmented%2Dbatch%5Fsize%3D128%2Dlr%3D2e%2D5%2Dmax%5Fgloss%3D6&ga=1

	Sense2Vector - https://github.com/explosion/sense2vec/releases/download/v1.0.0/s2v_reddit_2015_md.tar.gz

	Download and place these models inside 'models' directory.
	Bert-WSD should be in 'models/bert_base-augmented-batch_size=128-lr=2e-5-max_gloss=6'
	Coref-spanBERT should be in 'models/coref-spanbert'
	Sense2Vector should be in 'models/s2v_old'


Dependencies:
	To install necessary dependencies run the following command:
	$ pip install -r requirements.txt

	Then, open python shell and run the following commands:
	>>> import nltk
	>>> nltk.download('wordnet')
	>>> nltk.download('omw-1.4')

	And run the following command to download spacy dataset
	$ python -m spacy download en_core_web_sm


Run:
	To generate question run the mcq_generator.py script inside mcq_generator directory.
	python mcq_generator.py --text <your-text>
	This will print the questions and their choices and answers.


Server:
	To start the server, run the following commands:
	(inside the server directory)
	$ export FLASK_APP=app.py
	$ export FLASK_ENV=development
	$ flask run

	Start a live server and run the webpage inside 'webpage' directory.


