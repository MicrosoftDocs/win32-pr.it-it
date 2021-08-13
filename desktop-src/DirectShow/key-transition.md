---
description: Transizione chiave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transizione chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fc5b905b1650b6db6bb98b542193160825b8bd6dd74626ef9bddc91b118118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397278"
---
# <a name="key-transition"></a>Transizione chiave

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

La transizione Key esegue la keying in base al valore RGB, al valore alfa, alla tonalità o alla luminanza.

L'immagine seguente illustra la transizione chiave:

![transizione della chiave](images/trans-key.png)

ID classe (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

Nome variabile CLSID: CLSID \_ DxtKey

Nome descrittivo: "DxtKey"

Proprietà



| Proprietà   | Type  | Intervallo valido           | Descrizione                                                                                                                                                                                                                                                | Si applica a                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Tonalità        | int   | 0–360                 | Valore della tonalità su cui eseguire la chiave.                                                                                                                                                                                                                             | Tonalità                            |
| Inverti     | BOOL  | **FALSE** o **TRUE** | Valore booleano che indica se invertire l'operazione predefinita della chiave. Se **FALSE,** i pixel nell'immagine sovrasso vengono resi trasparenti nel modo predefinito. Se **TRUE,** l'operazione viene invertita.                                                   | Chroma, Hue, Luminance, Nonred |
| KeyType    | int   | Vedere la sezione Osservazioni           | Specifica il tipo di chiave. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                                                                                                              | Tutti                            |
| Luminance  | int   | 0–100                 | Valore di luminance su cui eseguire la chiave.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0 : 0xFFFFFF        | Colore su cui eseguire la chiave. Il valore è un numero esadecimale con formato 0x *RRGGBB*, dove *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. (Rosso puro, verde e blu sono 0xFF0000, 0x00FF00 e 0x0000FF, rispettivamente. | Chroma                         |
| Similarity | int   | 0–100                 | Intervallo di dati di colore che diventa trasparente. Con valori più elevati, una gamma più ampia di colori simili è trasparente.                                                                                                                                        | Chroma, Nonred                 |



 

## <a name="remarks"></a>Commenti

Il tipo di chiave eseguita dipende dal valore della proprietà **KeyType,** che deve essere uno dei seguenti:



| Valore | Enumerazione       | Descrizione                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Chiave chroma (chiave per valore RGB).                        |
| 1     | DXTKEY \_ NONRED    | Chiave non ritirata. Rende trasparenti le aree blu e verdi. |
| 2     | DXTKEY \_ LUMINANCE | Chiave di luminanza.                                        |
| 3     | DXTKEY \_ ALPHA     | Chiave per valore alfa.                                   |
| 4     | TONALITÀ DXTKEY \_       | Chiave per tonalità.                                           |



 

Per impostazione predefinita, il tipo di chiave è DXTKEY \_ ALPHA.

 

 



