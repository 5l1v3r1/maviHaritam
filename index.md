<!DOCTYPE html>
<html>
  <head>
    <meta charset='utf-8' />
    <title>v1.1</title>
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=yes ">
    <link href="https://fonts.googleapis.com/css?family=Josefin+Sans|Open+Sans:100,400,600,700,800,900&display=swap" rel="stylesheet">
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v1.6.0/mapbox-gl.js'></script>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v1.6.0/mapbox-gl.css' rel='stylesheet' />
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" type="text/css" href="styles2.css">
    <script type="text/javascript" src="firstScript.js"></script>
    <script type="text/javascript">
       // First we get the viewport height and we multiple it by 1% to get a value for a vh unit
       let vh = window.innerHeight * 0.01;
       // Then we set the value in the --vh custom property to the root of the document
       document.documentElement.style.setProperty('--vh', `${vh}px`);

       window.addEventListener('resize', () => {
       // We execute the same script as before
       let vh = window.innerHeight * 0.01;
       document.documentElement.style.setProperty('--vh', `${vh}px`);
       });
     </script>
  </head>
  <body>
    <div id="mapSpace">
      <div id='map'></div>
      <img id="zoomBalance" src="zoomBalance.svg">
      <div class = "rectangle"></div>     <!-- Top rectangle for styling -->
      <img id="logo" src="logo.svg">
      <button onclick="toggleSidebar()" id = "menuBtn"><i class="fa fa-bars"></i> Menu</button>
      <button id = "infoBtn" data-toggle="modal" data-target=".infoTab"><i class="fa fa-info"></i> Info</button>
      <div id="sidebar">
        <button onclick="closeSidebar()" id = "menuClose" class= "close">&times;</button>
        <ul>
         <li class="menu_li" id = "menuFirstItem" data-toggle="modal" data-target=".amac">Mavi Haritam Hakkında</li>
         <li class="menu_li" data-toggle="modal" data-target=".nedenOnemli">Atık Alımı Neden Önemli?</li>
         <li class="menu_li" data-toggle="modal" data-target=".yonetmelikler">Türkiye Karasuları İçin Atık Yönetmelikleri</li>
         <li class="menu_li" data-toggle="modal" data-target=".iletisim">İletişim</li>
         <li class="menu_li"> TR / EN </li>
        </ul>
      </div>
    </div>

<!-- __________________________MENU MODAL__________________________ -->
  <!-- MaviHarita'nın Amacı -->
  <div class="modal fade amac" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-l" role="document">
      <div class="modal-content">
        <button type="button" class="close menuModalClose" data-dismiss="modal">&times;</button>
        <h2 class="modalHeading">Mavi Haritam</h2>
        <div class="modal-innerContent">
          <p class = "modal_p">Mavi Haritam’ı, Türk karasularında bulunan sıvı atık alım tesislerinin denizciler tarafından öğrenilmesi, denetlenmesi, geliştirilmesi ve kullanımlarının arttırılması amacıyla hayata geçirdik.</p>
          <p class = "modal_p">Dileğimiz, denizlerdeki problemlerin inovatif fikirler ile çözülmesine yardımcı olacak bir platform olmak. </p> <br>
          <h4 class="amac_h">Mavi Haritam’ın başlıca amaçları: </h4>
          <ol>
            <li class = "amac_li">Denizcilere atık alım tesislerinin yeri, fiyatı ve telefon numaraları gibi temel bilgileri sunmak</li>
            <li class = "amac_li">Yorumlar ve halka açık geribildirimler sayesinde işletmelerin hizmet kalitesini arttırmak</li>
            <li class = "amac_li">Denizlerde atık yönetiminin önemi hakkında güvenilir bir bilgi kaynağı oluşturmak ve farkındalık yaratmak</li>
            <li class = "amac_li">Atık alım tesislerinin yetersiz olduğu bölgeleri harita üzerinde görünür kılmak ve çözüm için ses birliği oluşturmak</li>
            <li class = "amac_li">Denizlerimizdeki atık yönetimi kanunları hakkında denizcileri bilgilendirmek</li>
          </ol>
          <br>
          <div>
            <h1 class = "modal_h">V1.1 Hakkında</h1>
            <p class = "modal_p">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
            quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
            consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
            cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
            proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
            <br>
            <h1 class = "modal_h">Üstünde Çalıştığımız Geliştirmeler</h1>
            <p class = "modal_p" style="margin-bottom: 0.5em">Atık alım işletmelerini kullanan denizcilerin, işletmeler hakkında yorum yapıp puanlayabilecekleri bir sistem üzerinde çalışıyoruz.</p>
            <p class = "modal_p">Bunun, işletmeleri hem müşterilerine hem de paydaşlarına karşı daha şeffaf hale getirerek hizmet standartlarını yükselteceğine inanıyoruz.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
<!-- Aık Alımı Neden Önemli? -->
  <div class="modal fade nedenOnemli" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-xl" role="document">
      <div class="modal-content">
        <button type="button" class="close menuModalClose" data-dismiss="modal">&times;</button>
        <h2 class="modalHeading">Atık Alımı Neden Önemli?</h2>
        <div class="modal-innerContent">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum. <br>

          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum. <br>

          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum. <br>

          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum. <br>
        </div>
      </div>
    </div>
  </div>
  <!-- Türkiye'deki Atık Yönetmelikleri -->
  <div class="modal fade yonetmelikler" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-xl" role="document">
      <div class="modal-content">
        <button type="button" class="close menuModalClose" data-dismiss="modal">&times;</button>
        <h2 class="modalHeading">Türkiye Karasuları İçin Atık Yönetmelikleri</h2>
        <div class="modal-innerContent">
          !!!!Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </div>
    </div>
  </div>
  <!-- İletişim -->
  <div class="modal fade iletisim" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-l" role="document">
      <div class="modal-content">
        <button type="button" class="close menuModalClose" data-dismiss="modal">&times;</button>
        <h2 class="modalHeading">İletişim</h2>
        <div class="modal-innerContent">
          <p id = "iletisimModal_p">Paylaşım ve doğa sevgisine inanan denizciler olarak, gelişmek ve beraberce büyümek adına; soru, görüş ve önerileriniz bizim için çok önemli. <br><br>
          Bize ulaşmak için <a href="mailto:info@maviharitam.com">info@maviharitam.com</a> adresine Email atabilirsiniz. <br><br>
          Temiz, sağlıklı ve mavi denizlerde görüşmek üzere!</p> 
        </div>
      </div>
    </div>
  </div>

<!-- __________________________INFO MODAL__________________________ -->
  <!-- INFO -->
  <div class="modal fade infoTab" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg" role="document">
      <div class="modal-content">
        <button type="button" class="close" id="infoClose" data-dismiss="modal">&times;</button>
        <h2>Info</h2>
            <div id="infoArea">
              <span class="infoLine"><img src="pump1.svg" class="infoGraphic infoPumpImg"> <p class="infoText">İşletmede vakum pompası var*</p></span>
              <span class="infoLine"><img src="pump0.svg" class="infoGraphic infoPumpImg"> <p class="infoText">İşletmede vakum pompası yok*</p></span>
              <span class="infoLine"><img src="water1.svg" class="infoGraphic infoWaterImg"><p class="infoText">Tatlı su bağlantısı var</p></span>
              <span class="infoLine"><img src="water0.svg" class="infoGraphic infoWaterImg"><p class="infoText">Tatlı su bağlantısı yok</p></span>
              <span class="infoLine"><img src="ac1.svg" class="infoGraphic infoAcImg"><p class="infoText">220V bağlantısı var</p></span>
              <span class="infoLine"><img src="ac0.svg" class="infoGraphic infoAcImg"><p class="infoText">220V bağlantısı yok</p></span>
              <span class="infoLine"><img src="address.svg" class="infoGraphic" id="infoAddressImg"><p class="infoText">Koordinatlar <br>(Enlem,Boylam)</p></span>
              <span class="infoLine"><img src="contacts.svg" class="infoGraphic" id="infoContactsImg"><p class="infoText">Tesislerin telefon numaraları</p></span>
              <span class="infoLine"><img src="vhf.svg" class="infoGraphic" id="infoVhfImg"><p class="infoText">Telsiz frekans bilgisi</p></span>
              <span class="infoLine"><img src="grocery.svg" class="infoGraphic" id="infoGroceryImg"><p class="infoText">Yakınında market var</p></span>
              <span class="infoLine"><img src="medic.svg" class="infoGraphic" id="infoMedicImg"><p class="infoText">Yakınında eczane var</p></span>
              <span class="infoLine"><img src="food.svg" class="infoGraphic" id="infoFoodImg"><p class="infoText">Yakınında restoran var</p></span>
              <p id="extraInfo">* Vakum pompası olmayan işletmeler, sadece kendi imkanları ile atık verebilen teknelere hizmet verebilir. Vakum ünitesine ihtiyaç duyan tekneler "Vakum pompası var" işaretine sahip işletmeleri kullanmalıdır. <br>
              **Çoğu işletmede, tankı 1 tondan küçük olan teknelerden 1 ton fiyatı alınmaktadır.</p>
          </div>
      </div>
    </div>
  </div>

  

    <script type="text/javascript" src="mavijava.js"></script>
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
    <script type="text/javascript">
      document.getElementById("map").addEventListener('click', closeSidebar);

      function balanceZoom() {
        map.flyTo({
        center: [29.0, 39.000],
        zoom: zoomLevel, 
        })
      }

      var balanceButton = document.getElementById("zoomBalance")
      balanceButton.addEventListener("click", balanceZoom);
    </script>
  </body>
</html>