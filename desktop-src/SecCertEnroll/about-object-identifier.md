---
description: Il tipo di dati identificatore oggetto viene codificato in una tripletta TLV che inizia con un valore di tag 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICATORE OGGETTO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231508"
---
# <a name="object-identifier"></a><span data-ttu-id="5242c-103">IDENTIFICATORE OGGETTO</span><span class="sxs-lookup"><span data-stu-id="5242c-103">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="5242c-104">Il tipo di dati **identificatore oggetto** viene codificato in una tripletta TLV che inizia con un valore di **tag** 0x06.</span><span class="sxs-lookup"><span data-stu-id="5242c-104">The **OBJECT IDENTIFIER** data type is encoded into a TLV triplet that begins with a **Tag** value of 0x06.</span></span> <span data-ttu-id="5242c-105">Ogni numero intero di un identificatore di oggetto decimale punteggiato (OID) viene codificato in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="5242c-105">Each integer of a dotted decimal object identifier (OID) is encoded according to the following rules:</span></span>

-   <span data-ttu-id="5242c-106">I primi due nodi dell'OID sono codificati su un solo byte.</span><span class="sxs-lookup"><span data-stu-id="5242c-106">The first two nodes of the OID are encoded onto a single byte.</span></span> <span data-ttu-id="5242c-107">Il primo nodo viene moltiplicato per il numero decimale 40 e il risultato viene aggiunto al valore del secondo nodo.</span><span class="sxs-lookup"><span data-stu-id="5242c-107">The first node is multiplied by the decimal 40 and the result is added to the value of the second node.</span></span>
-   <span data-ttu-id="5242c-108">I valori dei nodi minori o uguali a 127 sono codificati in un byte.</span><span class="sxs-lookup"><span data-stu-id="5242c-108">Node values less than or equal to 127 are encoded on one byte.</span></span>
-   <span data-ttu-id="5242c-109">I valori del nodo maggiori o uguali a 128 vengono codificati su più byte.</span><span class="sxs-lookup"><span data-stu-id="5242c-109">Node values greater than or equal to 128 are encoded on multiple bytes.</span></span> <span data-ttu-id="5242c-110">Il bit 7 del byte più a sinistra è impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="5242c-110">Bit 7 of the leftmost byte is set to one.</span></span> <span data-ttu-id="5242c-111">I bit da 0 a 6 di ogni byte contengono il valore codificato.</span><span class="sxs-lookup"><span data-stu-id="5242c-111">Bits 0 through 6 of each byte contains the encoded value.</span></span>

<span data-ttu-id="5242c-112">Questi punti vengono mostrati nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5242c-112">These points are shown by the following illustration.</span></span>

![codifica der del tipo di dati identificatore oggetto](images/der-tlv-oid.png)

<span data-ttu-id="5242c-114">Nell'esempio seguente viene illustrato il modo in cui l'attributo **ClientID** viene codificato in una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="5242c-114">The following example shows how the **ClientId** attribute is encoded in a certificate request.</span></span>

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 



