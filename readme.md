<h2 style="text-align:center">YAPAY SİNİR AĞLARI İLE MEME KANSERİ TEŞHİSİ</h2>
<center><img src="https://i.hizliresim.com/b5j28me.jpeg"></center>

<h3>1. Giriş</h3>
<p>Meme kanseri, kadınlar arasında ikinci ölüm nedenidir. Erken teşhis ve ardından uygun kanser tedavisi ölümcül riski azaltabilir. Tümörler iyi veya kötü huylu olabilir. İyi huylu tümörler kanser değildir. Meme kanseri kötü huylu bir tümördür ve göğüs hücrelerinde gelişir.</p>

Tıp uzmanları bir hastalığı tespit ederken hata yapabilir. Veri madenciliği ve makine öğrenimi gibi teknolojinin yardımı, teşhis doğruluğunu önemli ölçüde artırabilir. Yapay Sinir Ağları (YSA), akıllı meme kanseri teşhisinde yaygın olarak kullanılmaktadır.

<hr></hr>

<h3>Yapay Sinir Ağları (Artificial Neural Network (ANN))</h3>
<p>Yapay sinir ağları insan beyni örnek alınarak, öğrenme sürecinin matematiksel olarak modellenmesi sonucu ortaya çıkmıştır. Beyindeki biyolojik sinir ağlarının yapısını, öğrenme, hatırlama ve genelleme kabiliyetlerini taklit eder.</p>


<center><img src="https://i.hizliresim.com/35n47ff.jpeg"></center>

YSA, sınıflandırma ve regresyon problemleri gibi yaygın veri madenciliği görevleri, örüntü tanıma, tıbbi teşhis, makine öğrenimi ve yapay zeka gibi çeşitli alanlarda akıllı bir araç olarak yaygın bir şekilde kullanılmaktadır.

<br/><ul><h4><b>Yapay Sinir Ağlarının Özellikleri</b></h4>

<li>Yapay sinir ağları, birçok hücreden meydana gelir ve bu hücreler eş zamanlı çalışarak karmaşık işleri gerçekleştirir.</li>
<li>Öğrenme kabiliyeti olduğundan farklı öğrenme algoritmalarıyla öğrenebilir.  </li>
<li>YSA, görülmemiş çıktılar için sonuç (bilgi) üretir.</li>
<li>Örüntü tanıma ve sınıflandırma yapma ve eksik örüntüleri tamamlayabilme özellikleri vardır.</li>
<li>Hata toleransına sahiptir.</li>
<li>Eksik veya belirsiz bilgiyle çalışabilir. Hatalı durumlarda dereceli bozulma(graceful degradation) gösterir. </li>
<li>Ek olarak paralel çalışabilmekte ve gerçek zamanlı bilgiyi işleyebilmektedir.</li>

</ul>
<p>Yapay sinir ağları başlıca teşhis, sınıflandırma, tahmin, kontrol, veri ilişkilendirme, veri filtreleme, yorumlama gibi alanlarda kullanılmaktadır. Hangi problem için hangi ağın daha uygun olduğunu belirlerken ağların özellikleri ile problemlerin özelliklerini karşılaştırmak gerekir.</p>

<p>Meme kanserinin sınıflandırılması, araştırmacılar ve bilim adamları için büyük bir zorluk oluşturan tıbbi bir uygulamadır. Birçok araştırma, YSA'nın meme kanseri teşhisinde iyi bir doğruluk sağladığını gösterdi.</p><br/>

<hr></hr>

<h3><b>3. Veri Kümesi</b></h3>

Bu çalışmada sınıflandırma testi doğruluğunu, hassasiyet ve özgüllük değerlerini ölçerek sunmakta olan <b>Wisconsin Meme Kanseri Teşhisi (WDBC)</b> veri kümesi kullanılmaktadır.

Kullanılan veri kümesi, UCI Makine Öğrenme Deposundaki 569 örnek ve 32 özellikten oluşan WDBC veri kümesidir. Veri kümesinde yer alan özelliklerden bazıları şunlardır:


<table height="300px" width="600px">
      <tr>
         <td><b>her hücre çekirdeği için yarıçap</td>
         <td>radius_mean</td>
         <td>radius_se</td>
         <td>radius_worst</td>
      </tr>
      <tr>
         <td><b>doku</b></td>
         <td>texture_mean</td>
         <td>texture_se</td>
         <td>texture_worst</td>
      </tr>
      <tr>
        <td><b>çevre</b></td>
        <td>perimeter_mean</td>
        <td>perimeter_se</td>
        <td>perimeter_worst</td>
      </tr>
      <tr>
        <td><b>alan</b></td>
        <td>area_mean</td>
        <td>area_se</td>
        <td>area_worst</td>
      </tr>
      <tr>
        <td><b>pürüzsüzlük</b></td>
        <td>smoothness_mean</td>
        <td>smoothness_se</td>
        <td>smoothness_worst</td>
      </tr>
      <tr>
        <td><b>kompaktlık</b></td>
        <td>compactness_mean</td>
        <td>compactness_se</td>
        <td>compactness_worst</td>
      </tr>
      <tr>
        <td><b>içbükeylik</b></td>
        <td>concavity_mean</td>
        <td>concavity_se</td>
        <td>concavity_mean</td>
      </tr>
      <tr>
        <td><b>içbükey noktalar</b></td>
        <td>concave points_mean</td>
        <td>concave points_se</td>
        <td>concave points_worst</td>
      </tr>
      <tr>
        <td><b>simetri</b></td>
        <td>symmetry_mean</td>
        <td>symmetry_se</td>
        <td>symmetry_worst</td>
      </tr>
      <tr>
        <td><b>fraktal boyutu</b></td>
        <td>fractal_dimension_mean</td>
        <td>fractal_dimension_se</td>
        <td>fractal_dimension_worst</td>
      </tr>
</table>

gibi özellikler bulunmaktadır. Veri kümesindeki 569 meme kanseri verisinin <b>212'si kötü huylu(malignant)</b> ve <b>357'si iyi huylu(benign)</b> idi.

<hr></hr>

<h3>4. Projenin Çalıştırılması</h3>

<a href="https://github.com/melikeoguz/breast-cancer-detection-with-deep-learning/blob/main/ann-binary-classification.ipynb"><button class="favorite styled" type="button" >Projeyi Görüntülemek İçin Tıklayınız !</button></a>



