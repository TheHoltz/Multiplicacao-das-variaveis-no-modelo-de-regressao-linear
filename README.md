# Objetivo  
O objetivo deste mini artigo é analisar os reflexos da multiplicação de uma variável regressora e de uma variável resposta em um modelo de regressão linear.

# Introdução 
Com a alvorada do avanço tecnológico e estatístico dos últimos tempos, os modelos de regressão linear já são empregados em diversas vertentes do conhecimento, tornando-o multidisciplinar. Uma questão pertinente a todos é o comportamento do modelo ao se multiplicar suas variáveis por constantes, cujo é um objeto de estudo de suma relevância principalmente á vertentes de aplicação econômica e física, onde são costantes as conversões de valores.

## PROVA FORMAL
### Conceitos iniciais
Inicialmente é importante conceituar que a multiplicação de qualquer variável por uma constante $k_{1}$, resulta na multiplicação de sua média por $k_{1}$:
$\bar{x} = \frac{1}{n}\sum_{i=1}^{n}x_{i} \rightarrow \frac{1}{n}\sum_{i=1}^{n}( k_{1} * x_{i}) \rightarrow k_{1} \frac{1}{n} \sum_{i=1}^{n}x_{i} \rightarrow k_{1} * \bar{x}$

Temos também que:
$$\hat\beta_{1} = \frac{\sum_{i=1}^{n}(x_{i}-  \bar{x})(y_{i}-\bar{y})}{\sum_{i=1}^{n}(x_{i}-\bar{x})^2} \Leftrightarrow \frac{\sum_{i=1}^{n}(x_{i}-  \bar{x})y_{i}}{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}$$\newline \newline \newline \newline \newline \newline \newline \newline

### Coeficiente $\hat\beta_{1}$ do novo modelo
Sendo assim ao multiplicarmos **$x$ por uma constante $k_{1}$** e **$y$ por uma constante $k_{2}$**, teremos o seguinte resultado:

$$\hat\beta_{1}' = \frac{\sum_{i=1}^{n}(k_{1}*x_{i}- k_{1} *\bar{x}) (k_{2} * y_{i})}{\sum_{i=1}^{n}(k_{1}*x_{i}-k_{1}*\bar{x})^2} \rightarrow$$
$$\frac{(k_{1})*\sum_{i=1}^{n}(x_{i}-\bar{x})(k_{2} * y_{i})}{(k_{1})^2 *\sum_{i=1}^{n}(x_{i}-\bar{x})^2} \rightarrow \frac{k_{2}* \hat\beta_{1}'}{k_{1}}$$ 

### Coeficiente $\hat\beta_{0}$ do novo modelo
Diante o exposto anterior, pode-se observar que $\hat\beta_{0}$ haverá alterações, o que pode ser conferido abaixo:
$$\hat\beta_{0}' =  \bar{y} + \hat\beta_{1}'\bar{x} \to k_{2}*\bar{y} + \frac{k_{2} * \hat\beta_{1}'}{k_{1}}* k_{1} * \bar{x} \rightarrow k_{2} * \bar{y} + k_{2} * \hat\beta_{1}'\bar{x} = k_{2} * \hat\beta_{0}'$$

### Estimações do novo modelo
$$\hat{y}_{i}' = k_{2}\hat\beta_{0}' + \frac{k_{2}}{k_{1}}\hat\beta_{1}*k_{1}*x_{i}\rightarrow k_{2} * (\hat\beta_{0}' + \hat\beta_{1}'x_{i}) \to k_{2} * \hat{y}_{i}'$$

### Residuos do novo modelo
$$e_{i}' = \sum_{i=1}^{n} (k_{2} * y_{i} - k_{2} * \hat{y}_{i}')^2 \to k_{2}^{2}* \sum_{i=1}^{n} (y_{i} - \hat{y}_{i}')^2$$

### Erro puro do novo modelo
$$e_{puro}' = \sum_{i=1}^{n} (k_{2} * y_{i} - k_{2} * \bar{y})^2 \to k_{2}^{2} * \sum_{i=1}^{n} (y_{i} - \bar{y})^2$$

### Coeficiente de determinação do novo modelo
$$R^2 = \frac{k_{2}^{2} * \sum_{i=1}^{n} (y_{i} - \hat{y}_{i}')^2}{k_{2}^{2} * \sum_{i=1}^{n} (y_{i} - \bar{y})^2} \to \frac{\sum_{i=1}^{n}(y_{i} - \hat{y}_{i}')^2}{\sum_{i=1}^{n}(y_{i} - \bar{y})^2}$$

***
#Conclusão
Indubitavelmente, conclui-se que o coeficiente de determinação do modelo não haverá alterações.

# Referências
AOGSTA. Changing units of measurement in a simple regression model. 2015. Disponível em: <https://bit.ly/2IBQTor>. Acesso em: 27 maio 2018.  
