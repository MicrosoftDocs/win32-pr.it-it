---
description: Il tipo di dati OBJECT IDENTIFIER viene codificato in una tripletta TLV che inizia con un valore Tag 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICATORE DI OGGETTO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35c2bf64424fa158eef3c666743142d5ec5a65108e3def28c43194d2eaf5adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903790"
---
# <a name="object-identifier"></a>IDENTIFICATORE DI OGGETTO

Il **tipo di dati OBJECT IDENTIFIER** viene codificato in una tripletta TLV che inizia con un valore **Tag** 0x06. Ogni numero intero di un identificatore di oggetto decimale virgola (OID) viene codificato in base alle regole seguenti:

-   I primi due nodi dell'OID vengono codificati in un singolo byte. Il primo nodo viene moltiplicato per il separatore decimale 40 e il risultato viene aggiunto al valore del secondo nodo.
-   I valori dei nodi minori o uguali a 127 vengono codificati in un byte.
-   I valori dei nodi maggiori o uguali a 128 vengono codificati su più byte. Il bit 7 del byte più a sinistra è impostato su uno. I bit da 0 a 6 di ogni byte contengono il valore codificato.

Questi punti sono illustrati nella figura seguente.

![Codifica der del tipo di dati dell'identificatore di oggetto](images/der-tlv-oid.png)

L'esempio seguente illustra come **l'attributo ClientId** viene codificato in una richiesta di certificato.

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

 

 



