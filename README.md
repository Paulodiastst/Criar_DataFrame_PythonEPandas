# CRIAR e MANIPULAR DATAFRAMES com Python PANDAS


```python
import numpy as np
import pandas as pd
```


```python
df1 = pd.DataFrame([44, 55, 66], ['Arroz', 'Feijão', 'Batata'], ['Quantidade'])
df1
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Quantidade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Arroz</th>
      <td>44</td>
    </tr>
    <tr>
      <th>Feijão</th>
      <td>55</td>
    </tr>
    <tr>
      <th>Batata</th>
      <td>66</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.DataFrame([[44, 55, 66], [77, 88, 99]], ['Arroz', 'Feijão'], ['Jan', 'Fev', 'Mar'])
df2
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Arroz</th>
      <td>44</td>
      <td>55</td>
      <td>66</td>
    </tr>
    <tr>
      <th>Feijão</th>
      <td>77</td>
      <td>88</td>
      <td>99</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2['Jan']
```




    Arroz     44
    Feijão    77
    Name: Jan, dtype: int64




```python
df2['Abr'] = df2['Mar'] - df2['Jan']
df2
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
      <th>Abr</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Arroz</th>
      <td>44</td>
      <td>55</td>
      <td>66</td>
      <td>22</td>
    </tr>
    <tr>
      <th>Feijão</th>
      <td>77</td>
      <td>88</td>
      <td>99</td>
      <td>22</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros = pd.DataFrame(np.random.randint(3000, 25000, size=(8, 12)),
                    ['Fiat', 'Pegeout', 'Volkswagem', 'Ford', 'Nissan', 'Toyota', 'Honda', 'Chevrolet'],
                    ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez'],)
carros
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
      <th>Abr</th>
      <th>Mai</th>
      <th>Jun</th>
      <th>Jul</th>
      <th>Ago</th>
      <th>Set</th>
      <th>Out</th>
      <th>Nov</th>
      <th>Dez</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fiat</th>
      <td>11348</td>
      <td>24594</td>
      <td>10774</td>
      <td>18636</td>
      <td>12250</td>
      <td>22505</td>
      <td>11038</td>
      <td>8597</td>
      <td>9097</td>
      <td>8516</td>
      <td>3582</td>
      <td>8218</td>
    </tr>
    <tr>
      <th>Pegeout</th>
      <td>4306</td>
      <td>21754</td>
      <td>17958</td>
      <td>17025</td>
      <td>3640</td>
      <td>21060</td>
      <td>8179</td>
      <td>20663</td>
      <td>5168</td>
      <td>23994</td>
      <td>14820</td>
      <td>22375</td>
    </tr>
    <tr>
      <th>Volkswagem</th>
      <td>21159</td>
      <td>24634</td>
      <td>8634</td>
      <td>11506</td>
      <td>22914</td>
      <td>15565</td>
      <td>14589</td>
      <td>16265</td>
      <td>20443</td>
      <td>13954</td>
      <td>14728</td>
      <td>15875</td>
    </tr>
    <tr>
      <th>Ford</th>
      <td>6166</td>
      <td>9594</td>
      <td>8654</td>
      <td>7978</td>
      <td>20140</td>
      <td>4506</td>
      <td>3654</td>
      <td>8825</td>
      <td>19466</td>
      <td>23794</td>
      <td>4158</td>
      <td>10817</td>
    </tr>
    <tr>
      <th>Nissan</th>
      <td>16519</td>
      <td>14006</td>
      <td>11659</td>
      <td>10110</td>
      <td>19338</td>
      <td>19910</td>
      <td>8497</td>
      <td>8200</td>
      <td>3050</td>
      <td>19382</td>
      <td>10894</td>
      <td>23564</td>
    </tr>
    <tr>
      <th>Toyota</th>
      <td>23830</td>
      <td>21070</td>
      <td>24464</td>
      <td>10003</td>
      <td>9104</td>
      <td>14423</td>
      <td>15999</td>
      <td>6302</td>
      <td>20345</td>
      <td>8689</td>
      <td>16987</td>
      <td>6738</td>
    </tr>
    <tr>
      <th>Honda</th>
      <td>15038</td>
      <td>11147</td>
      <td>22613</td>
      <td>13256</td>
      <td>18929</td>
      <td>8928</td>
      <td>3799</td>
      <td>18462</td>
      <td>19332</td>
      <td>8448</td>
      <td>6942</td>
      <td>10437</td>
    </tr>
    <tr>
      <th>Chevrolet</th>
      <td>11724</td>
      <td>13902</td>
      <td>7982</td>
      <td>13154</td>
      <td>11803</td>
      <td>7202</td>
      <td>9773</td>
      <td>16846</td>
      <td>11040</td>
      <td>7667</td>
      <td>17619</td>
      <td>9880</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros['Total'] = carros.sum(axis = 1)
carros
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
      <th>Abr</th>
      <th>Mai</th>
      <th>Jun</th>
      <th>Jul</th>
      <th>Ago</th>
      <th>Set</th>
      <th>Out</th>
      <th>Nov</th>
      <th>Dez</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fiat</th>
      <td>11348</td>
      <td>24594</td>
      <td>10774</td>
      <td>18636</td>
      <td>12250</td>
      <td>22505</td>
      <td>11038</td>
      <td>8597</td>
      <td>9097</td>
      <td>8516</td>
      <td>3582</td>
      <td>8218</td>
      <td>149155</td>
    </tr>
    <tr>
      <th>Pegeout</th>
      <td>4306</td>
      <td>21754</td>
      <td>17958</td>
      <td>17025</td>
      <td>3640</td>
      <td>21060</td>
      <td>8179</td>
      <td>20663</td>
      <td>5168</td>
      <td>23994</td>
      <td>14820</td>
      <td>22375</td>
      <td>180942</td>
    </tr>
    <tr>
      <th>Volkswagem</th>
      <td>21159</td>
      <td>24634</td>
      <td>8634</td>
      <td>11506</td>
      <td>22914</td>
      <td>15565</td>
      <td>14589</td>
      <td>16265</td>
      <td>20443</td>
      <td>13954</td>
      <td>14728</td>
      <td>15875</td>
      <td>200266</td>
    </tr>
    <tr>
      <th>Ford</th>
      <td>6166</td>
      <td>9594</td>
      <td>8654</td>
      <td>7978</td>
      <td>20140</td>
      <td>4506</td>
      <td>3654</td>
      <td>8825</td>
      <td>19466</td>
      <td>23794</td>
      <td>4158</td>
      <td>10817</td>
      <td>127752</td>
    </tr>
    <tr>
      <th>Nissan</th>
      <td>16519</td>
      <td>14006</td>
      <td>11659</td>
      <td>10110</td>
      <td>19338</td>
      <td>19910</td>
      <td>8497</td>
      <td>8200</td>
      <td>3050</td>
      <td>19382</td>
      <td>10894</td>
      <td>23564</td>
      <td>165129</td>
    </tr>
    <tr>
      <th>Toyota</th>
      <td>23830</td>
      <td>21070</td>
      <td>24464</td>
      <td>10003</td>
      <td>9104</td>
      <td>14423</td>
      <td>15999</td>
      <td>6302</td>
      <td>20345</td>
      <td>8689</td>
      <td>16987</td>
      <td>6738</td>
      <td>177954</td>
    </tr>
    <tr>
      <th>Honda</th>
      <td>15038</td>
      <td>11147</td>
      <td>22613</td>
      <td>13256</td>
      <td>18929</td>
      <td>8928</td>
      <td>3799</td>
      <td>18462</td>
      <td>19332</td>
      <td>8448</td>
      <td>6942</td>
      <td>10437</td>
      <td>157331</td>
    </tr>
    <tr>
      <th>Chevrolet</th>
      <td>11724</td>
      <td>13902</td>
      <td>7982</td>
      <td>13154</td>
      <td>11803</td>
      <td>7202</td>
      <td>9773</td>
      <td>16846</td>
      <td>11040</td>
      <td>7667</td>
      <td>17619</td>
      <td>9880</td>
      <td>138592</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros['Origem'] = ['Italia', 'França', 'Alemanha', 'EUA', 'Japão', 'Japão', 'Japão', 'EUA']
```


```python
carros
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
      <th>Abr</th>
      <th>Mai</th>
      <th>Jun</th>
      <th>Jul</th>
      <th>Ago</th>
      <th>Set</th>
      <th>Out</th>
      <th>Nov</th>
      <th>Dez</th>
      <th>Total</th>
      <th>Origem</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fiat</th>
      <td>11348</td>
      <td>24594</td>
      <td>10774</td>
      <td>18636</td>
      <td>12250</td>
      <td>22505</td>
      <td>11038</td>
      <td>8597</td>
      <td>9097</td>
      <td>8516</td>
      <td>3582</td>
      <td>8218</td>
      <td>149155</td>
      <td>Italia</td>
    </tr>
    <tr>
      <th>Pegeout</th>
      <td>4306</td>
      <td>21754</td>
      <td>17958</td>
      <td>17025</td>
      <td>3640</td>
      <td>21060</td>
      <td>8179</td>
      <td>20663</td>
      <td>5168</td>
      <td>23994</td>
      <td>14820</td>
      <td>22375</td>
      <td>180942</td>
      <td>França</td>
    </tr>
    <tr>
      <th>Volkswagem</th>
      <td>21159</td>
      <td>24634</td>
      <td>8634</td>
      <td>11506</td>
      <td>22914</td>
      <td>15565</td>
      <td>14589</td>
      <td>16265</td>
      <td>20443</td>
      <td>13954</td>
      <td>14728</td>
      <td>15875</td>
      <td>200266</td>
      <td>Alemanha</td>
    </tr>
    <tr>
      <th>Ford</th>
      <td>6166</td>
      <td>9594</td>
      <td>8654</td>
      <td>7978</td>
      <td>20140</td>
      <td>4506</td>
      <td>3654</td>
      <td>8825</td>
      <td>19466</td>
      <td>23794</td>
      <td>4158</td>
      <td>10817</td>
      <td>127752</td>
      <td>EUA</td>
    </tr>
    <tr>
      <th>Nissan</th>
      <td>16519</td>
      <td>14006</td>
      <td>11659</td>
      <td>10110</td>
      <td>19338</td>
      <td>19910</td>
      <td>8497</td>
      <td>8200</td>
      <td>3050</td>
      <td>19382</td>
      <td>10894</td>
      <td>23564</td>
      <td>165129</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Toyota</th>
      <td>23830</td>
      <td>21070</td>
      <td>24464</td>
      <td>10003</td>
      <td>9104</td>
      <td>14423</td>
      <td>15999</td>
      <td>6302</td>
      <td>20345</td>
      <td>8689</td>
      <td>16987</td>
      <td>6738</td>
      <td>177954</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Honda</th>
      <td>15038</td>
      <td>11147</td>
      <td>22613</td>
      <td>13256</td>
      <td>18929</td>
      <td>8928</td>
      <td>3799</td>
      <td>18462</td>
      <td>19332</td>
      <td>8448</td>
      <td>6942</td>
      <td>10437</td>
      <td>157331</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Chevrolet</th>
      <td>11724</td>
      <td>13902</td>
      <td>7982</td>
      <td>13154</td>
      <td>11803</td>
      <td>7202</td>
      <td>9773</td>
      <td>16846</td>
      <td>11040</td>
      <td>7667</td>
      <td>17619</td>
      <td>9880</td>
      <td>138592</td>
      <td>EUA</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 8 entries, Fiat to Chevrolet
    Data columns (total 14 columns):
     #   Column  Non-Null Count  Dtype 
    ---  ------  --------------  ----- 
     0   Jan     8 non-null      int32 
     1   Fev     8 non-null      int32 
     2   Mar     8 non-null      int32 
     3   Abr     8 non-null      int32 
     4   Mai     8 non-null      int32 
     5   Jun     8 non-null      int32 
     6   Jul     8 non-null      int32 
     7   Ago     8 non-null      int32 
     8   Set     8 non-null      int32 
     9   Out     8 non-null      int32 
     10  Nov     8 non-null      int32 
     11  Dez     8 non-null      int32 
     12  Total   8 non-null      int64 
     13  Origem  8 non-null      object
    dtypes: int32(12), int64(1), object(1)
    memory usage: 576.0+ bytes
    


```python
carros.describe()
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Fev</th>
      <th>Mar</th>
      <th>Abr</th>
      <th>Mai</th>
      <th>Jun</th>
      <th>Jul</th>
      <th>Ago</th>
      <th>Set</th>
      <th>Out</th>
      <th>Nov</th>
      <th>Dez</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>8.00000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>13761.250000</td>
      <td>17587.625000</td>
      <td>14092.250000</td>
      <td>12708.500000</td>
      <td>14764.750000</td>
      <td>14262.375000</td>
      <td>9441.000000</td>
      <td>13020.000000</td>
      <td>13492.625000</td>
      <td>14305.500000</td>
      <td>11216.250000</td>
      <td>13488.000000</td>
      <td>162140.12500</td>
    </tr>
    <tr>
      <th>std</th>
      <td>6786.598617</td>
      <td>6094.703413</td>
      <td>6641.364979</td>
      <td>3628.483036</td>
      <td>6595.011811</td>
      <td>6774.512928</td>
      <td>4471.740058</td>
      <td>5589.837616</td>
      <td>7257.773683</td>
      <td>7103.685563</td>
      <td>5683.181824</td>
      <td>6425.376254</td>
      <td>23889.33818</td>
    </tr>
    <tr>
      <th>min</th>
      <td>4306.000000</td>
      <td>9594.000000</td>
      <td>7982.000000</td>
      <td>7978.000000</td>
      <td>3640.000000</td>
      <td>4506.000000</td>
      <td>3654.000000</td>
      <td>6302.000000</td>
      <td>3050.000000</td>
      <td>7667.000000</td>
      <td>3582.000000</td>
      <td>6738.000000</td>
      <td>127752.00000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>10052.500000</td>
      <td>13213.250000</td>
      <td>8649.000000</td>
      <td>10083.250000</td>
      <td>11128.250000</td>
      <td>8496.500000</td>
      <td>7084.000000</td>
      <td>8497.750000</td>
      <td>8114.750000</td>
      <td>8499.000000</td>
      <td>6246.000000</td>
      <td>9464.500000</td>
      <td>146514.25000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>13381.000000</td>
      <td>17538.000000</td>
      <td>11216.500000</td>
      <td>12330.000000</td>
      <td>15589.500000</td>
      <td>14994.000000</td>
      <td>9135.000000</td>
      <td>12545.000000</td>
      <td>15186.000000</td>
      <td>11321.500000</td>
      <td>12811.000000</td>
      <td>10627.000000</td>
      <td>161230.00000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>17679.000000</td>
      <td>22464.000000</td>
      <td>19121.750000</td>
      <td>14198.250000</td>
      <td>19538.500000</td>
      <td>20197.500000</td>
      <td>11925.750000</td>
      <td>17250.000000</td>
      <td>19685.750000</td>
      <td>20485.000000</td>
      <td>15361.750000</td>
      <td>17500.000000</td>
      <td>178701.00000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>23830.000000</td>
      <td>24634.000000</td>
      <td>24464.000000</td>
      <td>18636.000000</td>
      <td>22914.000000</td>
      <td>22505.000000</td>
      <td>15999.000000</td>
      <td>20663.000000</td>
      <td>20443.000000</td>
      <td>23994.000000</td>
      <td>17619.000000</td>
      <td>23564.000000</td>
      <td>200266.00000</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros.columns
```




    Index(['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out',
           'Nov', 'Dez', 'Total', 'Origem'],
          dtype='object')




```python
carros[['Jan', 'Abr', 'Origem']]
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jan</th>
      <th>Abr</th>
      <th>Origem</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fiat</th>
      <td>11348</td>
      <td>18636</td>
      <td>Italia</td>
    </tr>
    <tr>
      <th>Pegeout</th>
      <td>4306</td>
      <td>17025</td>
      <td>França</td>
    </tr>
    <tr>
      <th>Volkswagem</th>
      <td>21159</td>
      <td>11506</td>
      <td>Alemanha</td>
    </tr>
    <tr>
      <th>Ford</th>
      <td>6166</td>
      <td>7978</td>
      <td>EUA</td>
    </tr>
    <tr>
      <th>Nissan</th>
      <td>16519</td>
      <td>10110</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Toyota</th>
      <td>23830</td>
      <td>10003</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Honda</th>
      <td>15038</td>
      <td>13256</td>
      <td>Japão</td>
    </tr>
    <tr>
      <th>Chevrolet</th>
      <td>11724</td>
      <td>13154</td>
      <td>EUA</td>
    </tr>
  </tbody>
</table>
</div>




```python
carros.index
```




    Index(['Fiat', 'Pegeout', 'Volkswagem', 'Ford', 'Nissan', 'Toyota', 'Honda',
           'Chevrolet'],
          dtype='object')


