---
description: Transizione della chiave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transizione della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876202"
---
# <a name="key-transition"></a>Transizione della chiave

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

La transizione della chiave esegue la digitazione in base al valore RGB, al valore alfa, alla tonalità o alla luminosità.

Nell'immagine seguente viene illustrata la transizione della chiave:

![transizione della chiave](images/trans-key.png)

ID classe (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

Nome variabile CLSID: CLSID \_ DxtKey

Nome descrittivo: "DxtKey"

Proprietà



| Proprietà   | Type  | Intervallo valido           | Descrizione                                                                                                                                                                                                                                                | Si applica a                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Tonalità        | INT   | 0 – 360                 | Valore di tonalità su cui eseguire la chiave.                                                                                                                                                                                                                             | Tonalità                            |
| Inverti     | BOOL  | **False** o **true** | Valore booleano che indica se invertire l'operazione predefinita della chiave. Se **false**, i pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito. Se **true**, l'operazione viene invertita.                                                   | Chroma, Hue, Luminance, Nonred |
| KeyType    | INT   | Vedere la sezione Osservazioni           | Specifica il tipo di chiave. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                                                                                                              | Tutti                            |
| Luminance  | INT   | 0 – 100                 | Valore di luminanza su cui eseguire la chiave.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0-0xFFFFFF        | Colore su cui eseguire la chiave. Il valore è un numero esadecimale con formato 0x *RRGGBB*, dove *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. I puri rossi, verdi e blu sono rispettivamente 0xFF0000, 0x00FF00 e 0x0000FF. | Croma                         |
| Similarity | INT   | 0 – 100                 | Intervallo di dati del colore che diventa trasparente. Con valori superiori, una gamma più ampia di colori simili è trasparente.                                                                                                                                        | Chroma, Nonred                 |



 

## <a name="remarks"></a>Commenti

Il tipo di chiave eseguita dipende dal valore della proprietà del **tipo** di chiave, che deve essere uno dei seguenti:



| Valore | Enumerazione       | Descrizione                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Chroma Key (chiave per valore RGB).                        |
| 1     | \_NONRED DXTKEY    | Chiave di Nonred. (Rende trasparenti le aree blu e verde). |
| 2     | \_luminanza DXTKEY | Chiave di luminanza.                                        |
| 3     | DXTKEY \_ alfa     | Chiave per valore alfa.                                   |
| 4     | \_tonalità DXTKEY       | Chiave per tonalità.                                           |



 

Il valore predefinito del tipo di chiave è DXTKEY \_ alfa.

 

 



