---
description: I valori integer sono codificati in una tripletta TLV che inizia con un valore di Tag pari a 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEGER (API di registrazione certificati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345436"
---
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="1b1ea-103">INTEGER (API di registrazione certificati)</span><span class="sxs-lookup"><span data-stu-id="1b1ea-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="1b1ea-104">I valori integer sono codificati in una tripletta TLV che inizia con un valore di **tag** pari a 0x02.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="1b1ea-105">Il campo del **valore** della terna di TLV contiene l'intero codificato se è positivo o il complemento a due se è negativo.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="1b1ea-106">Se il valore integer è positivo, ma il bit di ordine superiore è impostato su 1, viene aggiunto un 0x00 di primo livello al contenuto per indicare che il numero non è negativo.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="1b1ea-107">Ad esempio, il byte di ordine elevato di 0x8F (10001111) è 1.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="1b1ea-108">Viene pertanto aggiunto al contenuto un byte zero iniziali, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![codifica der del tipo di dati Boolean](images/der-tlv-integer.png)

<span data-ttu-id="1b1ea-110">Se il valore integer contiene meno di 128 byte, il campo *length* richiede un solo byte per specificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="1b1ea-111">Se il valore integer è maggiore di 127 byte, il bit 7 del campo *length* è impostato su 1 e BITS 6-0 specifica il numero di byte aggiuntivi utilizzati per identificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="1b1ea-112">Per ulteriori informazioni, vedere [lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="1b1ea-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="1b1ea-113">Nell'esempio seguente, da [ \# ASN 10 con codifica ASN. 1](pkcs--10-encoded-asn-1.md), viene visualizzata la codifica per una chiave pubblica a 128 byte.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="1b1ea-114">Il primo byte contiene il valore del **tag** per il tipo di dati **Integer** , 0x02.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="1b1ea-115">Il secondo e il terzo byte contengono il valore **length** .</span><span class="sxs-lookup"><span data-stu-id="1b1ea-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="1b1ea-116">Il bit 7 del secondo byte è impostato su 1 perché sono presenti più di 127 byte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="1b1ea-117">I bit da 0 a 6 del secondo byte specificano il numero di byte finali necessari, in questo caso uno, per specificare accuratamente la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="1b1ea-118">Il terzo byte specifica il numero di byte di contenuto, 0x81.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="1b1ea-119">Il quarto byte, 0x00, viene aggiunto al contenuto per indicare che l'intero è effettivamente un valore positivo anche se il bit di segno del byte di contenuto iniziali (0x8F) è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

<span data-ttu-id="1b1ea-120">Nell'esempio seguente viene illustrato come codificare il valore integer 0x03.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="1b1ea-121">Il byte di **tag** contiene 0x02 e la **lunghezza** byte indica che è presente un byte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b1ea-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="1b1ea-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b1ea-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b1ea-123">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="1b1ea-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="1b1ea-124">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="1b1ea-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



