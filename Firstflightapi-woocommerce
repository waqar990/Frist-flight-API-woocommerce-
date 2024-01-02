<?php

//ben curl yöntemini kullandım farklı yöntemler kullanabilirsiniz Erhan.

   $aliciulke = $_POST['aliciulke'];

   $ulkem = explode ('|', $aliciulke);

   $ulkekod = $ulkem[1];

   $firmaad = $_POST['firmaad'];

   $aliciad = $_POST['aliciad'];

   $aliciadres = $_POST['aliciadres'];

   $alicisehir = $_POST['alicisehir'];

   $postakod = $_POST['postakod'];

   $alicitel = $_POST['alicitel'];

   

   $referans = $_POST['num'];

   $gonderi = $_POST['gonderi'];

   $telefon = $_POST['telefon'];

   $icerik = $_POST['icerik'];

   

   $ad = $_POST['ad'];

   $firma = $_POST['firma'];

   $uyeadres = $_POST['uyeadres'];

   $sehir = $_POST['sehir'];

   $postakodu = $_POST['postakodu'];

   $tel = $_POST['tel'];

   
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://ontrack.firstflightme.com/FFCService.svc/CreateAirwayBill',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{

  "AirwayBillData": {

    "AirWayBillCreatedBy": "",

    "CODAmount": "10",

    "CODCurrency": "TRY",

    "Destination": "DXB",

    "DutyConsigneePay": "0",

    "GoodsDescription": "CARGO",

    "NumberofPeices": 1,

    "Origin": "TUO",

    "ProductType": "XPS",

    "ReceiversAddress1": "'.$aliciadres.'",

    "ReceiversAddress2": "",

    "ReceiversCity": "'.$alicisehir.'",

    "ReceiversSubCity": "",

    "ReceiversCountry": "'.$ulkekod.'",

    "ReceiversCompany": "'.$firmaad.'",

    "ReceiversContactPerson": "'.$aliciad.'",

    "ReceiversEmail": "alicim4994yz@mail.com",

    "ReceiversGeoLocation": "",

    "ReceiversMobile": "'.$alicitel.'",

    "ReceiversPhone": "'.$alicitel.'",

    "ReceiversPinCode": "400001",

    "ReceiversProvince": "",

    "SendersAddress1": "'.$uyeadres.'",

    "SendersAddress2": "'.$postakodu.'",

    "SendersCity": "'.$sehir.'",

    "SendersSubCity ": "",

    "SendersCountry": "TR",

    "SendersCompany": "'.$firma.'",

    "SendersContactPerson": "'.$ad.'",

    "SendersEmail": "sirket@mail.com.tr",

    "SendersGeoLocation": "",

    "SendersMobile": "'.$tel.'",

    "SendersPhone": "'.$tel.'",

    "SendersPinCode": "",

    "ServiceType": "CAD",

    "ShipmentDimension": "1X1X1",

    "ShipmentInvoiceCurrency": "USD",

    "ShipmentInvoiceValue": 10,

    "ShipperReference": "'.$referans.'",

    "ShipperVatAccount": "",

    "SpecialInstruction": "",

    "Weight": 1

  },

  "UserName": "kullanıcı adınınız.",

  "Password": "sifreniz",

  "AccountNo": "numaranız",

  "Country": "TR"

}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));


$result = json_decode(curl_exec($curl),true);


curl_close($curl);
echo $response;

$refno = $result['AirwayBillNumber'];

echo $refno;

header("location: dubak.php?id=$telefon&refno=$refno");


?>
