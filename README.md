# URL FakeNews Checker

### Rodar diretamente  
```
git clone https://github.com/caesarcc/python-tcc-url-fakenews-check.git
cd python-tcc-url-fakenews-check
docker-compose up
```

### Rodar em ambiente local (pip venv em ambiente windows)  
```
python -m venv venv
.\venv\Scripts\activate
python -m pip install --upgrade pip
pip install --no-cache-dir -r requirements.txt
flask run
```

### Rodar em ambiente local (conda em ambiente windows, sem GPU)  
```
conda create --name tcc python=3.8
conda activate tcc
pip install --no-cache-dir -r requirements.txt
flask run
```

### Antes de rodar os notebooks do projeto localmente:
```
conda activate tcc
conda install pytorch torchvision torchaudio cpuonly -c pytorch
conda install -c huggingface transformers
conda install -c conda-forge ipywidgets
jupyter nbextension enable --py widgetsnbextension
```

<BR>  

## Roadmap:  

- [ ] Treinar modelo com Huggeface e BERT no FakeBR.Corpus:    
    - Projeto base: https://www.thepythoncode.com/article/fake-news-classification-in-python?utm_source=newsletter&utm_medium=email&utm_campaign=newsletter
    - Fake.Br Corpus: https://github.com/roneysco/Fake.br-Corpus  
    - BERTimbau: https://github.com/neuralmind-ai/portuguese-bert
    - Huggeface: https://huggingface.co/transformers/pretrained_models.html  
<HR>

- [ ] Implementar a captura da URL e limpar o texto:  
    - Lib para screaping de Artigos: https://newspaper.readthedocs.io/en/latest/
    - Lib para screaping quando anterior falhar: https://www.analyticsvidhya.com/blog/2021/04/automate-web-scraping-using-python-autoscraper-library/
    - Lib Normalizar dados: https://github.com/thalesbertaglia/enelvo
<HR>

- [ ] Sumarizar a notícia para apresentar:
    - Sumarizar com transformers: https://www.thepythoncode.com/article/text-summarization-using-huggingface-transformers-python
    
    - Sumarizar com Gensim: https://www.geeksforgeeks.org/python-extractive-text-summarization-using-gensim/
    - WordEmbedding para gensim: http://nilc.icmc.usp.br/nilc/index.php/repositorio-de-word-embeddings-do-nilc
    - Text Sumarization com nltk e gensim: https://towardsdatascience.com/a-better-approach-to-text-summarization-d7139b571439 e https://github.com/gaetangate/text-summarizer
<HR>

- [ ] Executar modelo (primeiro item) na notícia sumarizada (último item):
<HR>

- [ ] Apresentar resultado e gerar opção de CONFIRMAR FAKE ou VERDADE:
    - Tentar conferir se o modelo não está enviezado por poucas palavras: https://www.kaggle.com/code/josutk/only-one-word-99-2  
<HR>

- [ ] Gerar base de questões resolvidas e exportar para novo treinamento:
<HR>

## PASSOS OPCIONAIS ##

- [ ] Analizar o sentimento da notícia:
    - Análise de sentimentos baseada em regras: https://www.analyticsvidhya.com/blog/2021/06/rule-based-sentiment-analysis-in-python/
<HR>

- [ ] Conferir quantidade de erros na notícia original:
    - Spell Cheking: https://www.youtube.com/watch?v=rjXeG0aT-7w
<HR>

- [ ] Realizar pesquisa no Google sobre o assunto da notícia:
    - Pesquisar no Google: https://www.youtube.com/watch?v=IBhdLRheKyM
<HR>

- [ ] Incrementar o corpus de treino com mais dados: 
    - Lib Autoscraping com modelado: https://www.analyticsvidhya.com/blog/2021/04/automate-web-scraping-using-python-autoscraper-library/
    - Lib Normalizar dados: https://github.com/thalesbertaglia/enelvo
    - Fakewhatsapp corpus: https://github.com/cabrau/FakeWhatsApp.Br
    - Notícias do Lupa: https://piaui.folha.uol.com.br/lupa/2022/04/19/verificamos-trf-drogas-traficantes/
    - Notícias do G1: https://g1.globo.com/fato-ou-fake/
    - Boatos: https://www.boatos.com.br/
<HR>

- Projeto de detecção de fake news parado: https://jornal.usp.br/ciencias/ciencias-exatas-e-da-terra/ferramenta-para-detectar-fake-news-e-desenvolvida-pela-usp-e-pela-ufscar/ e https://nilc-fakenews.herokuapp.com/about

- Explicação de Lematização: https://www.alura.com.br/artigos/lemmatization-vs-stemming-quando-usar-cada-uma
- Explicação sobre a Bertimbau: https://neuralmind.ai/2020/11/29/bertimbau-da-neuralmind-e-recordista-em-downloads/

- Projeto antigo no Kaggle: https://www.kaggle.com/code/aishwarya2210/prediction-of-fake-news-model-comparison

- Ferramentas para NLP em PT-BR: 
https://medium.com/turing-talks/ferramentas-para-processamento-de-linguagem-natural-em-portugu%C3%AAs-977c7f59c382
