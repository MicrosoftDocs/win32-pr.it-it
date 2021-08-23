---
description: La proprietà KaraokeAudioPresentationMode imposta o recupera la combinazione di altoparlanti di destra a sinistra per i canali ausiliari per il glossario.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Proprietà KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af634a3beaade7e497cdc6d158ccf1121ebb09542bdec92ceaae823b1b91ccdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952380"
---
# <a name="karaokeaudiopresentationmode-property"></a>Proprietà KaraokeAudioPresentationMode

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La proprietà imposta o recupera la combinazione di altoparlanti di destra a sinistra per i canali `KaraokeAudioPresentationMode` ausiliari per il tutto.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero contenente un set di flag di bit che indicano come i canali ausiliari del disacco ai parlanti sinistro e destro vengono downmix.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con un valore predefinito pari a zero.

I canali audio sono in base zero, quindi i canali 0 e 1 rappresentano in genere i canali del parlante destro e sinistro e i canali da 2 a 4 sono i tre canali ausiliari per il perno. Quando l'oggetto MSWebDVD entra in modalità tutto schermo, disattiva automaticamente i canali 2 e versioni successive. Usare operazioni **OR** bit per bit per impostare il bit appropriato per inviare un canale ausiliario al parlante sinistro, al parlante destro, a entrambi gli altoparlanti (entrambi i bit) o a nessun parlante (entrambi i bit disattivati). Questi bit sono tutti disattivati per impostazione predefinita ogni volta che lo strumento di spostamento DVD entra in modalità tutto schermo. Il valore dei bit e l'azione corrispondente sono riportati nella tabella seguente.



| Valore  | Descrizione                            |
|--------|----------------------------------------|
| 0x0004 | Downmix Channel 2 a sinistra  |
| 0x0008 | Downmix Channel 3 a sinistra  |
| 0x0010 | Downmix Channel 4 a sinistra  |
| 0x0400 | Downmix Channel 2 al parlante destro |
| 0x0800 | Downmix Channel 3 al parlante destro |
| 0x1000 | Downmix Channel 4 al parlante destro |



 

 

 



