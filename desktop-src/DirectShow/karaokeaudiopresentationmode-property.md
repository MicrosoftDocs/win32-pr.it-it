---
description: La proprietà KaraokeAudioPresentationMode imposta o recupera la combinazione di altoparlanti a destra sinistra per i canali karaoke ausiliari.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Proprietà KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303810"
---
# <a name="karaokeaudiopresentationmode-property"></a>Proprietà KaraokeAudioPresentationMode

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `KaraokeAudioPresentationMode` proprietà imposta o recupera la combinazione di altoparlanti a destra sinistra per i canali karaoke ausiliari.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore integer contenente un set di flag di bit che indica il modo in cui i canali karaoke ausiliari vengono riprodottoti agli altoparlanti sinistro e destro.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è zero.

I canali audio sono in base zero, quindi i canali 0 e 1 rappresentano in genere i canali speaker destro e sinistro e i canali da 2 a 4 sono i tre canali karaoke ausiliari. Quando l'oggetto MSWebDVD entra in modalità karaoke, disattiva automaticamente i canali 2 e versioni successive. Utilizzare operazioni **OR bit per bit** per impostare il bit appropriato in modo da inviare un canale ausiliario all'altoparlante sinistro, all'altoparlante destro, a entrambi gli altoparlanti (entrambi i bit) o a nessun altoparlante (entrambi BITS). Questi bit sono tutti spenti per impostazione predefinita ogni volta che il navigatore DVD entra in modalità karaoke. Il valore dei bit e la relativa azione corrispondente sono indicati nella tabella seguente.



| Valore  | Descrizione                            |
|--------|----------------------------------------|
| 0x0004 | Canale 2 downmix a sinistra  |
| 0x0008 | Downmix Channel 3 (altoparlante a sinistra)  |
| 0x0010 | Downmix Channel 4 (altoparlante a sinistra)  |
| 0x0400 | Downmix Channel 2 nell'altoparlante destro |
| 0x0800 | Downmix Channel 3 nell'altoparlante destro |
| 0x1000 | Downmix Channel 4 nell'altoparlante destro |



 

 

 



