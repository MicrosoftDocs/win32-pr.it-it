---
description: Il tipo di dati stringa di BIT è codificato in una tripletta TLV che inizia con un byte di tag di 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: STRINGA DI BIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557376"
---
# <a name="bit-string"></a><span data-ttu-id="6ed0c-103">STRINGA DI BIT</span><span class="sxs-lookup"><span data-stu-id="6ed0c-103">BIT STRING</span></span>

<span data-ttu-id="6ed0c-104">Il tipo di dati **stringa di bit** è codificato in una tripletta TLV che inizia con un byte di **tag** di 0x03.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-104">The **BIT STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x03.</span></span> <span data-ttu-id="6ed0c-105">Il campo del **valore** della tripletta TLV contiene un byte principale che specifica il numero di bit rimasti inutilizzati nel byte finale del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-105">The **Value** field of the TLV triplet contains a leading byte that specifies the number of bits left unused in the final byte of content.</span></span> <span data-ttu-id="6ed0c-106">Nell'esempio seguente il campo **length** è impostato su 0x03 perché seguono tre byte di contenuto e il byte di apertura del campo **value** è impostato su 0x04 perché sono presenti quattro bit inutilizzati nell'ultimo byte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-106">In the following example, the **Length** field is set to 0x03 because three content bytes follow, and the leading byte of the **Value** field is set to 0x04 because there are four unused bits in the last content byte.</span></span> <span data-ttu-id="6ed0c-107">Ogni bit inutilizzato è indicato dalla lettera x.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-107">Each unused bit is denoted by the letter x.</span></span>

![codifica der del tipo di dati stringa di bit](images/der-tlv-bitstring.png)

<span data-ttu-id="6ed0c-109">Nell'esempio seguente, adattato dall' [argomento \# ASN. 1 con codifica PKCS 10](pkcs--10-encoded-asn-1.md) , viene visualizzata la firma codificata di una richiesta di certificato PKCS 10 di esempio \# .</span><span class="sxs-lookup"><span data-stu-id="6ed0c-109">The following example, adapted from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows the encoded signature of a sample PKCS \#10 certificate request.</span></span> <span data-ttu-id="6ed0c-110">Il primo byte contiene il valore del **tag** per il tipo di dati **stringa di bit** 0x03.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-110">The first byte contains the **Tag** value for the **BIT STRING** data type, 0x03.</span></span> <span data-ttu-id="6ed0c-111">Il secondo e il terzo byte contengono la lunghezza della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-111">The second and third bytes contain the length of the byte array.</span></span> <span data-ttu-id="6ed0c-112">Il bit 7 del secondo byte è impostato su 1 perché sono presenti più di 127 byte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-112">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="6ed0c-113">I bit da 0 a 6 del secondo byte specificano il numero di byte di **lunghezza** finale, in questo caso uno.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-113">Bits 0 through 6 of the second byte specify the number of trailing **Length** bytes, in this case one.</span></span> <span data-ttu-id="6ed0c-114">Il terzo byte specifica il numero di byte di contenuto, 0x81.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-114">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="6ed0c-115">Il quarto byte, 0x00, specifica il numero di bit inutilizzati presenti nell'ultimo byte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-115">The fourth byte, 0x00, specifies the number of unused bits that exist in the last content byte.</span></span> <span data-ttu-id="6ed0c-116">Si noti che la firma è codificata in ordine di byte big-endian.</span><span class="sxs-lookup"><span data-stu-id="6ed0c-116">Note that the signature is encoded in big-endian byte order.</span></span>

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a><span data-ttu-id="6ed0c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ed0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed0c-118">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="6ed0c-118">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="6ed0c-119">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="6ed0c-119">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="6ed0c-120">Byte di lunghezza e valore codificati</span><span class="sxs-lookup"><span data-stu-id="6ed0c-120">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



