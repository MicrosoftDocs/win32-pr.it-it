---
description: L'elemento Group definisce un gruppo, ovvero l'oggetto di primo livello in una sequenza temporale.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965820"
---
# <a name="group-element"></a>Elemento Group

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'elemento **Group** definisce un gruppo, ovvero l'oggetto di primo livello in una sequenza temporale.

## <a name="attributes"></a>Attributi

[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**Height**](height-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Name**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**SamplingRate**](samplingrate-attribute.md), [**Type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**Width**](width-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Padre   | [**sequenza temporale**](timeline-element.md)                                                                     |
| Children | [**composto**](composite-element.md), [**effetto**](effect-element.md), [**traccia**](track-element.md) |



 

## <a name="remarks"></a>Commenti

All'interno di un `group` elemento, la priorità dei livelli annidati viene determinata in modo implicito in base all'ordine in cui vengono visualizzati all'interno dell'elemento. Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità sempre maggiori.

## <a name="examples"></a>Esempi


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



