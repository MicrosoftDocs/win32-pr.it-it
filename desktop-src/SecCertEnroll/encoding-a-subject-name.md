---
description: Quando si inizializza un oggetto IX500DistinguishedName con un nome distinto per identificare l'oggetto di una richiesta di certificato, viene creata una sequenza ASN.1 (Abstract Syntax Notation One) codificata Distinguished Encoding Rules (DER).
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Codifica di un nome soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8849bda237c174fb160c862da4399fa4a734dbc74b5e6f476e1c59d22d1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780080"
---
# <a name="encoding-a-subject-name"></a>Codifica di un nome soggetto

Quando si inizializza un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) con un nome distinto per identificare l'oggetto di una richiesta di certificato, viene creata una sequenza ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) codificata [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER). Si supponga, ad esempio, che il nome distinto del soggetto sia costituito dai nomi distinti relativi (RDN) seguenti:<dl> E=Administrator@jdomcsc.nttest.microsoft.com  
CN=Administrator  
CN=Users  
DC=jdomcsc  
DC=nttest  
DC=microsoft  
DC=com  
</dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 rinnovo codificato ASN.1.</a>

``` syntax
0a0d: 30 81 c4          ; SEQUENCE (c4 Bytes)
0a10: |  31 13          ; SET (13 Bytes)
0a12: |  |  30 11               ; SEQUENCE (11 Bytes)
0a14: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a16: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a20: |  |     16 03        ; IA5_STRING (3 Bytes)
0a22: |  |        63 6f 6d                                          ; com
      |  |           ; "com"
0a25: |  31 19          ; SET (19 Bytes)
0a27: |  |  30 17               ; SEQUENCE (17 Bytes)
0a29: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a2b: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a35: |  |     16 09            ; IA5_STRING (9 Bytes)
0a37: |  |        6d 69 63 72 6f 73 6f 66  74                       ; microsoft
      |  |           ; "microsoft"
0a40: |  31 16          ; SET (16 Bytes)
0a42: |  |  30 14               ; SEQUENCE (14 Bytes)
0a44: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a46: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a50: |  |     16 06            ; IA5_STRING (6 Bytes)
0a52: |  |        6e 74 74 65 73 74                                 ; nttest
      |  |           ; "nttest"
0a58: |  31 17          ; SET (17 Bytes)
0a5a: |  |  30 15               ; SEQUENCE (15 Bytes)
0a5c: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a5e: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a68: |  |     16 07            ; IA5_STRING (7 Bytes)
0a6a: |  |        6a 64 6f 6d 63 73 63                              ; jdomcsc
      |  |           ; "jdomcsc"
0a71: |  31 0e          ; SET (e Bytes)
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
0a81: |  31 16          ; SET (16 Bytes)
0a83: |  |  30 14               ; SEQUENCE (14 Bytes)
0a85: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a87: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a8a: |  |     13 0d            ; PRINTABLE_STRING (d Bytes)
0a8c: |  |        41 64 6d 69 6e 69 73 74  72 61 74 6f 72           ; Administrator
      |  |           ; "Administrator"
0a99: |  31 39          ; SET (39 Bytes)
0a9b: |     30 37               ; SEQUENCE (37 Bytes)
0a9d: |        06 09            ; OBJECT_ID (9 Bytes)
0a9f: |        |  2a 86 48 86 f7 0d 01 09  01
      |        |     ; 1.2.840.113549.1.9.1 Email Address (E)
0aa8: |        16 2a            ; IA5_STRING (2a Bytes)
0aaa: |           41 64 6d 69 6e 69 73 74  72 61 74 6f 72 40 6a 64  ; Administrator@jd
0aba: |           6f 6d 63 73 63 2e 6e 74  74 65 73 74 2e 6d 69 63  ; omcsc.nttest.mic
0aca: |           72 6f 73 6f 66 74 2e 63  6f 6d                    ; rosoft.com
      |              ; "Administrator@jdomcsc.nttest.microsoft.com"
```

Come illustrato in [Nomi soggetto](subject-names.md), ogni RDN in un nome distinto è costituito da un set di attributi e ogni attributo contiene un identificatore di oggetto (OID) e un valore. [](/windows/desktop/SecGloss/o-gly) Per comprendere in che modo [**l'oggetto IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) codifica un nome distinto, prendere in considerazione il nome comune CN=Users.

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

La sintassi di trasferimento DER di un oggetto ASN.1 contiene sempre un tipo, una lunghezza e una tripletta di valori e ogni campo nella tripletta contiene sempre uno o più byte. Quando viene codificato, CN=Users è costituito da un OID e da un valore stringa. La notazione decimale virgola dell'OID CN è 2.5.4.3 e il valore stringa è "Users". Il valore stringa è rappresentato come tipo **PRINTABLE_STRING** dati. Il valore del tipo numerico associato **OBJECT_ID** è sempre 0x06 e il tipo numerico associato a PRINTABLE_STRING **è** sempre 0x13. La lunghezza del nome comune "Users" è 0x05 byte. La lunghezza dell'OID 0x03 byte e il relativo valore è 0x55 0x04 0x03.

> [!Note]  
> Per convertire le prime due cifre dell'OID 2.5.4.3 nel valore esadecimale 0x55, moltiplicare la prima cifra dell'OID per 40 (2 x 40) e aggiungere la seconda cifra (5) prima della conversione in formato esadecimale.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PKCS \# 7 Renewal Encoded ASN.1](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[Richieste di esempio](sample-requests.md)
</dt> <dt>

[Nomi soggetto](subject-names.md)
</dt> </dl>

 

 
