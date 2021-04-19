---
description: Un SET contiene una serie non ordinata di campi di uno o più tipi.
ms.assetid: 6bbe89da-1177-4cfa-9515-03b271e5ef6b
title: SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572114d754b5034babe81e3914599f48996867d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311934"
---
# <a name="set"></a><span data-ttu-id="ba36f-103">SET</span><span class="sxs-lookup"><span data-stu-id="ba36f-103">SET</span></span>

<span data-ttu-id="ba36f-104">Un **set** contiene una serie non ordinata di campi di uno o più tipi.</span><span class="sxs-lookup"><span data-stu-id="ba36f-104">A **SET** contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="ba36f-105">Viene codificato in una tripletta TLV che inizia con un byte di **tag** di 0x31.</span><span class="sxs-lookup"><span data-stu-id="ba36f-105">It is encoded into a TLV triplet that begins with a **Tag** byte of 0x31.</span></span> <span data-ttu-id="ba36f-106">Nell'esempio seguente, adattato dall'argomento [ASN. 1 con codifica CMC](cmc-encoded-asn-1.md) , viene illustrato come un attributo **ClientID** è codificato in una struttura di dati **set** .</span><span class="sxs-lookup"><span data-stu-id="ba36f-106">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how a **ClientId** attribute is encoded in a **SET** data structure.</span></span> <span data-ttu-id="ba36f-107">L'attributo può essere specificato tramite l'interfaccia [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="ba36f-107">The attribute can be specified by using the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface.</span></span>

``` syntax
31 59                                     ; SET (59 Bytes)
   30 57                                  ; SEQUENCE (57 Bytes)
      06 09                               ; OBJECT_ID (9 Bytes)
      |  2b 06 01 04 01 82 37 15  14      ;   1.3.6.1.4.1.311.21.20 
      31 4a                               ; SET (4a Bytes)
         30 48                            ; SEQUENCE (48 Bytes)
            02 01                         ; INTEGER (1 Bytes)
            |  09
            0c 23                         ; UTF8_STRING (23 Bytes)
            |  76 69 63 68 33 64 2e 6a    ;   vich3d.j
            |  64 6f 6d 63 73 63 2e 6e    ;   domcsc.n
            |  74 74 65 73 74 2e 6d 69    ;   ttest.mi
            |  63 72 6f 73 6f 66 74 2e    ;   crosoft.
            |  63 6f 6d                   ;   com
            0c 15                         ; UTF8_STRING (15 Bytes)
            |  4a 44 4f 4d 43 53 43 5c    ;   JDOMCSC\
            |  61 64 6d 69 6e 69 73 74    ;   administ
            |  72 61 74 6f 72             ;   rator
            0c 07                         ; UTF8_STRING 
```

<span data-ttu-id="ba36f-108">Se il **set** contiene meno di 128 byte, il campo **lunghezza** della tripletta TLV richiede un solo byte per specificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ba36f-108">If the **SET** contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="ba36f-109">Se è maggiore di 127 byte, bit 7 del campo **lunghezza** è impostato su 1 e BITS 6-0 specifica il numero di byte aggiuntivi usati per identificare la lunghezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ba36f-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="ba36f-110">Per ulteriori informazioni, vedere [lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="ba36f-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba36f-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba36f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba36f-112">Sistema di tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ba36f-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="ba36f-113">Codifica DER dei tipi ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ba36f-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



