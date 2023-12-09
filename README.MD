
## <div class="header2">Structure </div>
- data/
  - raw/
    - cc.csv
  - processed/
    - cc_cluster.csv
- src/
  - `__`init__.py
  - cluster.py
- notebooks/
  - cluster.ipynb
- requirements.txt
- README.md



## <div class="header2">1 - Dataset Description</div>
<div class="explain-box"><b>Structure of the dataset</b>.<br>

<b> This case requires to develop a customer segmentation to define marketing strategy. The
sample Dataset summarizes the usage behavior of about 9000 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables.</b>

<i>Following is the Data Dictionary for Credit Card dataset:</i>
    
<table style="font-family: Merriweather; font-weight: 300; font-size: 12px; text-align: left; padding: 8px; border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th style="font-family: Merriweather; font-weight: 900; text-align: center; font-size: 14px">Nome da Variável</th>
      <th style="font-family: Merriweather; font-weight: 900; text-align: center; font-size: 14px">Descrição em Inglês</th>
      <th style="font-family: Merriweather; font-weight: 900; text-align: center; font-size: 14px">Descrição em Português</th>
    </tr>
  </thead>
  <tbody>
      <tr>
          <td>CUST_ID</td>
          <td>Identification of Credit Card holder (Categorical)</td>
          <td>Identificação do titular do cartão de crédito (Categórico)</td>
      </tr>
      <tr>
          <td>BALANCE</td>
          <td>Balance amount left in their account to make purchases</td>
          <td>Valor do saldo remanescente na conta para fazer compras</td>
      </tr>
      <tr>
          <td>BALANCE_FREQUENCY</td>
          <td>How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)</td>
          <td>Frequência com que o saldo é atualizado, pontuação entre 0 e 1 (1 = atualização frequente, 0 = atualização não frequente)</td>
      </tr>
      <tr>
          <td>PURCHASES</td>
          <td>Amount of purchases made from account</td>
          <td>Valor das compras feitas na conta</td>
      </tr>
      <tr>
          <td>ONEOFF_PURCHASES</td>
          <td>Maximum purchase amount done in one-go</td>
          <td>Valor máximo de compra feito de uma só vez</td>
      </tr>
      <tr>
          <td>INSTALLMENTS_PURCHASES</td>
          <td>Amount of purchase done in installment</td>
          <td>Valor das compras feitas em parcelas</td>
      </tr>
      <tr>
          <td>CASH_ADVANCE</td>
          <td>Cash in advance given by the user</td>
          <td>Adiantamento em dinheiro dado pelo usuário</td>
      </tr>
      <tr>
          <td>PURCHASES_FREQUENCY</td>
          <td>How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)</td>
          <td>Frequência com que as compras são feitas, pontuação entre 0 e 1 (1 = compras frequentes, 0 = compras não frequentes)</td>
      </tr>
      <tr>
          <td>ONEOFF_PURCHASES_FREQUENCY</td>
          <td>How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)</td>
          <td>Frequência das compras em uma única transação (1 = compras frequentes, 0 = compras não frequentes)</td>
      </tr>
      <tr>
          <td>PURCHASES_INSTALLMENTS_FREQUENCY</td>
          <td>How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)</td>
          <td>Frequência das compras em parcelas (1 = frequentes, 0 = não frequentes)</td>
      </tr>
      <tr>
          <td>CASH_ADVANCE_FREQUENCY</td>
          <td>How frequently the cash in advance being paid</td>
          <td>Frequência com que o adiantamento em dinheiro é pago</td>
      </tr>
      <tr>
          <td>CASH_ADVANCE_TRX</td>
          <td>Number of Transactions made with "Cash in Advanced"</td>
          <td>Número de transações feitas com "Adiantamento em Dinheiro"</td>
      </tr>
      <tr>
          <td>PURCHASES_TRX</td>
          <td>Number of purchase transactions made</td>
          <td>Número de transações de compra realizadas</td>
      </tr>
      <tr>
          <td>CREDIT_LIMIT</td>
          <td>Limit of Credit Card for user</td>
          <td>Limite do cartão de crédito para o usuário</td>
      </tr>
      <tr>
          <td>PAYMENTS</td>
          <td>Amount of Payment done by user</td>
          <td>Valor do pagamento feito pelo usuário</td>
      </tr>
      <tr>
          <td>MINIMUM_PAYMENTS</td>
          <td>Minimum amount of payments made by user</td>
          <td>Valor mínimo dos pagamentos feitos pelo usuário</td>
      </tr>
      <tr>
          <td>PRC_FULL_PAYMENT</td>
          <td>Percent of full payment paid by user</td>
          <td>Percentagem de pagamento total feito pelo usuário</td>
      </tr>
      <tr>
          <td>TENURE</td>
          <td>Tenure of credit card service for user</td>
          <td>Duração do serviço do cartão de crédito para o usuário</td>
      </tr>
  </tbody>
</table>




# Credit Card Customer Clustering Analysis

## 1. Initial Visualization:
- Started with a comprehensive visualization using histograms for various columns in the DataFrame to gain insights into the data distribution.

## 2. Normality Test (Shapiro-Wilk):
- Conducted the Shapiro-Wilk normality test to assess whether the variables follow a normal distribution.

## 3. Data Standardization:
- Standardized the data using the `StandardScaler` to ensure consistent scaling across all variables.

## 4. Hopkins Test:
- Applied the Hopkins test to evaluate the clustering tendency of the dataset.

## 5. Dimensionality Reduction (PCA):
- Utilized Principal Component Analysis (PCA) to reduce the data dimensionality to two principal components.

## 6. Determining the Number of Clusters (Elbow Method):
- Employed the Elbow method to determine the optimal number of clusters.

## 7. Application of K-Means:
- Applied the K-Means algorithm for the actual clustering process.

## 8. Results Visualization:
- Visualized the clustering results using a scatter plot and a waffle chart to represent the percentage distribution of each cluster.

## 9. Detailed Cluster Analysis:
- Conducted a detailed analysis of clusters, including the count of elements in each cluster and the percentage relative to the total.

## 10. Preparation for Feature Analysis:
- Prepared the data for feature analysis by removing certain columns and applying Min-Max normalization.

## 11. Detailed Feature Visualization by Cluster:
- Plotted histograms for each feature, separated by clusters, using `FacetGrid` to delve into the nuances of feature distributions.

In summary, this analysis delves into the underlying structure of the dataset, aiming to identify groups of credit card customers with similar characteristics through clustering techniques and detailed visualizations. The multi-step process involves data exploration, statistical testing, clustering, and a thorough examination of feature distributions within clusters.



# Conclusion

This project aimed to conduct a comprehensive analysis of credit card customers, using clustering techniques to identify patterns and similar characteristics. We began with data exploration and visualization, performed statistical tests to assess variable normality, standardized the data, and applied dimensionality reduction techniques such as PCA. Subsequently, we used the K-Means algorithm to cluster the customers.

The visualizations provided valuable insights into the distribution of clusters and the variation of characteristics among them. Additionally, the waffle chart analysis allowed for a graphical representation of the percentage distribution of each cluster.


