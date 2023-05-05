Download Link: https://assignmentchef.com/product/solved-cse225-project-1-text-representation-with-higher-order-paths
<br>
Advantages of using higher-order paths [1] between documents are illustrated in Fig. 1. In this figure, there are three documents, <em>d<sub>1</sub></em>, <em>d<sub>2</sub></em> and <em>d<sub>3</sub></em> which include a set of terms <em>{t<sub>1</sub>, t<sub>2,</sub> t<sub>3</sub>}, {t<sub>3</sub>, t<sub>4</sub>, t<sub>5</sub>} </em>and <em>{t<sub>4</sub>, t<sub>5</sub>}</em> respectively. Using a traditional similarity measure which is based on the shared terms (e.g. dot product), similarity value between documents <em>d<sub>1</sub></em> and <em>d<sub>3</sub></em> will be zero since they do not share any terms. But in fact these two documents have some similarities in the context of the dataset through <em>d<sub>2 </sub></em>as it can be seen in Fig. 1. This supports the idea that using higher-order paths between documents, it is possible to obtain a non-zero similarity value between <em>d<sub>1</sub></em> and <em>d<sub>3</sub></em> which was not possible in traditional Bag of Words (BOW) [2] representation. This value becomes larger if there are many interconnecting documents like <em>d<sub>2</sub></em> between <em>d<sub>1</sub></em> and <em>d<sub>3</sub></em>. This may stem from the reason that the two documents are written on the same topic using two different but semantically closer sets of terms.

This project aims to represent these higher-order paths by using <strong><em>Linked-Lists</em></strong>. Consequently, this project is a programming assignment in C, which aims to build an algorithm based on linked-lists that will build an efficient representation of documents.




<strong>Fig. 1.</strong> a) Illustration of higher-order paths




1<sup>st</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>2</sub>}, {t<sub>2</sub>, t<sub>3</sub>}, {t<sub>3</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>4</sub>}, {t<sub>4</sub>, t<sub>5</sub>}

2<sup>nd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>3</sub>}, {t<sub>1</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>5</sub>}, {t<sub>3</sub>, t<sub>5</sub>}

3<sup>rd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>5</sub>}




<strong>Fig. 2.</strong> b) Graphical demonstration of first-order, second-order and third-order paths between terms through documents




Your program needs to open and read text files under the following directories: econ, magazine and health. These are 3 categories of 1150Haber dataset [3]. The number of documents in these categories will be arbitrary. Furthermore, the number of terms in these documents will also be arbitrary.  In other words, the length of these files will be arbitrary.

Your program is expected to do the followings:

<ol>

 <li>a) (60 points) You need to read all the documents under all the categories. Then you need to build a Linked-List (MLL). Each node in this MLL needs to represent a different term in these documents. All the terms in these documents are expected to be in the MLL. There will be cases, the same word occur in different documents, or in the same document. Then, you do not need to add a term into the MLL if it already exists. In other words, be careful about not entering the duplicate records into the MLL. After reading and storing all your data into Linked list, you are expected to find 1<sup>st</sup>, 2<sup>nd</sup> and 3<sup>rd</sup> order term co-occurrences as shown below. <sub> </sub></li>

</ol>




1<sup>st</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>2</sub>}, {t<sub>2</sub>, t<sub>3</sub>}, {t<sub>3</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>4</sub>}, {t<sub>4</sub>, t<sub>5</sub>}

2<sup>nd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>3</sub>}, {t<sub>1</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>5</sub>}, {t<sub>3</sub>, t<sub>5</sub>}

3<sup>rd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>5</sub>}




There are several ways to build a suitable data structure by using Linked-List in order to find higher-order paths. <strong><em>In this project, you are also expected to write your algorithm’s analysis (i.e. Give the big-O time (order) of your code). </em></strong>

<strong> </strong>

<strong>Output: </strong>

1<sup>st</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>2</sub>}, {t<sub>2</sub>, t<sub>3</sub>}, {t<sub>3</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>4</sub>}, {t<sub>4</sub>, t<sub>5</sub>}

2<sup>nd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>3</sub>}, {t<sub>1</sub>, t<sub>4</sub>}, {t<sub>2</sub>, t<sub>5</sub>}, {t<sub>3</sub>, t<sub>5</sub>}

3<sup>rd</sup>-order term co-occurrence {t<sub>1</sub>, t<sub>5</sub>}




and




<strong><em>big-O time (order) of your code</em></strong>

<ol>

 <li>(20 points)</li>

</ol>

<strong>Output: </strong>Your program will output following information:

Most frequent 10 words in the input set of documents <strong><em>for each category</em></strong>, sorted descending by their term frequency (tf) coupled with their tf values. format, example:







<table width="262">

 <tbody>

  <tr>

   <td width="80"><strong>Econ </strong></td>

   <td width="98"><strong>Health </strong></td>

   <td width="84"><strong>Magazine </strong></td>

  </tr>

  <tr>

   <td width="80">Dolar,8</td>

   <td width="98">Operation,12</td>

   <td width="84">Cinema,24</td>

  </tr>

  <tr>

   <td width="80">Bank,7</td>

   <td width="98">Medicine,10</td>

   <td width="84">Actor,21</td>

  </tr>

  <tr>

   <td width="80">Strategy,6</td>

   <td width="98">Doctor,8</td>

   <td width="84">Theatre,18</td>

  </tr>

  <tr>

   <td width="80">…</td>

   <td width="98">…</td>

   <td width="84">…</td>

  </tr>

  <tr>

   <td width="80"> </td>

   <td width="98"> </td>

   <td width="84"> </td>

  </tr>

 </tbody>

</table>




<ol>

 <li></li>

</ol>

<strong>Output: </strong>Most frequent 10 words in the input set of documents <strong><em>for each category</em></strong>, sorted descending by their term frequency*inverse document frequency (idf) coupled with their tfidf values.




IDF (t) =log <sub>e </sub>N/n







<em>N</em>: Total number of documents  <em>n</em>: Number of documents with term t in it.




<table width="298">

 <tbody>

  <tr>

   <td width="92"><strong>Econ </strong></td>

   <td width="110"><strong>Health </strong></td>

   <td width="96"><strong>Magazine </strong></td>

  </tr>

  <tr>

   <td width="92">Dolar,1.8</td>

   <td width="110">Operation,2.12</td>

   <td width="96">Cinema,3.24</td>

  </tr>

  <tr>

   <td width="92">Bank,1.7</td>

   <td width="110">Medicine,2.10</td>

   <td width="96">Actor,3.21</td>

  </tr>

  <tr>

   <td width="92">Strategy,0.6</td>

   <td width="110">Doctor,1.8</td>

   <td width="96">Theatre,2.18</td>

  </tr>

  <tr>

   <td width="92">…</td>

   <td width="110">…</td>

   <td width="96">…</td>

  </tr>

  <tr>

   <td width="92"> </td>

   <td width="110"> </td>

   <td width="96"> </td>

  </tr>

 </tbody>

</table>





