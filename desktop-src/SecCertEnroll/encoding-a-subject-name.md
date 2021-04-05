---
description: Quando si Inizializza un oggetto IX500DistinguishedName con un nome distinto per identificare l'oggetto di una richiesta di certificato, viene creata una sequenza (ASN. 1) codificata con una sintassi di Distinguished Encoding Rules (DER).
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Codifica di un nome soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa03d95497a600c3e61fdda53820fd7a9858c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049583"
---
# <a name="encoding-a-subject-name"></a><span data-ttu-id="1346d-103">Codifica di un nome soggetto</span><span class="sxs-lookup"><span data-stu-id="1346d-103">Encoding a Subject Name</span></span>

<span data-ttu-id="1346d-104">Quando si Inizializza un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) con un nome distinto per identificare l'oggetto di una richiesta di certificato, viene creata una sequenza (ASN. 1) codificata con una [*sintassi*](/windows/desktop/SecGloss/a-gly) di [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="1346d-104">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object with a distinguished name to identify the subject of a certificate request, a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) sequence is created.</span></span> <span data-ttu-id="1346d-105">Si supponga, ad esempio, che il nome distinto del soggetto sia costituito dai nomi distinti relativi (RDNs) seguenti:</span><span class="sxs-lookup"><span data-stu-id="1346d-105">For example, assume that the subject distinguished name consists of the following relative distinguished names (RDNs):</span></span><dl> <span data-ttu-id="1346d-106">E =Administrator@jdomcsc.nttest.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1346d-106">E=Administrator@jdomcsc.nttest.microsoft.com</span></span>  
<span data-ttu-id="1346d-107">CN = amministratore</span><span class="sxs-lookup"><span data-stu-id="1346d-107">CN=Administrator</span></span>  
<span data-ttu-id="1346d-108">CN = utenti</span><span class="sxs-lookup"><span data-stu-id="1346d-108">CN=Users</span></span>  
<span data-ttu-id="1346d-109">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="1346d-109">DC=jdomcsc</span></span>  
<span data-ttu-id="1346d-110">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="1346d-110">DC=nttest</span></span>  
<span data-ttu-id="1346d-111">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="1346d-111">DC=microsoft</span></span>  
<span data-ttu-id="1346d-112">DC = com</span><span class="sxs-lookup"><span data-stu-id="1346d-112">DC=com</span></span>  
<span data-ttu-id="1346d-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">Un argomento di PKCS #7 Renewal encoded con codifica ASN. 1</a> .</span><span class="sxs-lookup"><span data-stu-id="1346d-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 Renewal Encoded ASN.1</a> topic.</span></span>

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

<span data-ttu-id="1346d-114">Come illustrato in [nomi di oggetto](subject-names.md), ogni RDN in un nome distinto è costituito da un set di attributi e ogni attributo contiene un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) e un valore.</span><span class="sxs-lookup"><span data-stu-id="1346d-114">As discussed in [Subject Names](subject-names.md), every RDN in a distinguished name consists of a set of attributes, and each attribute contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) and a value.</span></span> <span data-ttu-id="1346d-115">Per comprendere il modo in cui l'oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) codifica un nome distinto, prendere in considerazione il nome comune CN = Users.</span><span class="sxs-lookup"><span data-stu-id="1346d-115">To understand how the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object encodes a distinguished name, consider the common name CN=Users.</span></span>

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

<span data-ttu-id="1346d-116">La sintassi DER transfer di un oggetto ASN. 1 contiene sempre un tipo, una lunghezza e una tripletta del valore e ogni campo nella tripletta contiene uno o più byte.</span><span class="sxs-lookup"><span data-stu-id="1346d-116">The DER transfer syntax of an ASN.1 object always contains a type, length, and value triplet, and each field in the triplet contains one or more bytes.</span></span> <span data-ttu-id="1346d-117">Una volta codificato, CN = Users è costituito da un OID e da un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="1346d-117">When encoded, CN=Users consists of an OID and a string value.</span></span> <span data-ttu-id="1346d-118">La notazione decimale tratteggiata dell'OID CN è 2.5.4.3 e il valore della stringa è "Users".</span><span class="sxs-lookup"><span data-stu-id="1346d-118">The dotted decimal notation of the CN OID is 2.5.4.3 and the string value is "Users".</span></span> <span data-ttu-id="1346d-119">Il valore stringa è rappresentato come tipo di dati **PRINTABLE_STRING** .</span><span class="sxs-lookup"><span data-stu-id="1346d-119">The string value is represented as a **PRINTABLE_STRING** data type.</span></span> <span data-ttu-id="1346d-120">Il valore di tipo numerico associato a **object_id** è sempre 0x06 e il tipo numerico associato a **PRINTABLE_STRING** è sempre 0x13.</span><span class="sxs-lookup"><span data-stu-id="1346d-120">The numeric type value associated with **OBJECT_ID** is always 0x06, and the numeric type associated with **PRINTABLE_STRING** is always 0x13.</span></span> <span data-ttu-id="1346d-121">La lunghezza del nome comune "Users" è 0x05 bytes.</span><span class="sxs-lookup"><span data-stu-id="1346d-121">The length of the common name "Users" is 0x05 bytes.</span></span> <span data-ttu-id="1346d-122">La lunghezza dell'OID è 0x03 byte e il valore è 0x55 0x04 0x03.</span><span class="sxs-lookup"><span data-stu-id="1346d-122">The length of the OID is 0x03 bytes, and it's value is 0x55 0x04 0x03.</span></span>

> [!Note]  
> <span data-ttu-id="1346d-123">Per tradurre le prime due cifre dell'OID 2.5.4.3 nel valore esadecimale 0x55, moltiplicare la prima cifra dell'OID per 40 (2 x 40) e aggiungere la seconda cifra (5) prima della conversione in esadecimale.</span><span class="sxs-lookup"><span data-stu-id="1346d-123">To translate the first two digits of the OID 2.5.4.3 into the hexadecimal value 0x55, multiply the first digit of the OID by 40 (2 x 40) and add the second digit (5) before converting to hexadecimal.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1346d-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1346d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1346d-125">\#ASN con codifica del rinnovo PKCS 7.1</span><span class="sxs-lookup"><span data-stu-id="1346d-125">PKCS \#7 Renewal Encoded ASN.1</span></span>](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[<span data-ttu-id="1346d-126">Richieste di esempio</span><span class="sxs-lookup"><span data-stu-id="1346d-126">Sample Requests</span></span>](sample-requests.md)
</dt> <dt>

[<span data-ttu-id="1346d-127">Nomi soggetto</span><span class="sxs-lookup"><span data-stu-id="1346d-127">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 
