---
description: Il tipo di dati PrintableString ASN. 1 è codificato in una tripletta TLV che inizia con un byte di tag di 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881669"
---
# <a name="printablestring"></a><span data-ttu-id="baae0-103">PrintableString</span><span class="sxs-lookup"><span data-stu-id="baae0-103">PrintableString</span></span>

<span data-ttu-id="baae0-104">Il tipo di dati **PRINTABLESTRING** ASN. 1 è codificato in una tripletta TLV che inizia con un byte di **tag** di 0x13.</span><span class="sxs-lookup"><span data-stu-id="baae0-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="baae0-105">Nell'esempio seguente, dall'argomento [ \# ASN. 1 con codifica PKCS 10](pkcs--10-encoded-asn-1.md) , viene illustrato come un nome comune utente di TestCN sia codificato come tipo **PrintableString** .</span><span class="sxs-lookup"><span data-stu-id="baae0-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="baae0-106">L'identificatore di oggetto per un nome comune è 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="baae0-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="baae0-107">Se la stringa contiene meno di 128 byte, il campo **lunghezza** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="baae0-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="baae0-108">Se la stringa è maggiore di 127 byte, il bit 7 del campo **lunghezza** è impostato su 1 e BITS 6-0 specifica il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="baae0-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="baae0-109">Per ulteriori informazioni, vedere [lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="baae0-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="baae0-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="baae0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baae0-111">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="baae0-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="baae0-112">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="baae0-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



