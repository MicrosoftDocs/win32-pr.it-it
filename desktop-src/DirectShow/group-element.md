---
description: L'elemento group definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909249"
---
# <a name="group-element"></a>Elemento group

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

**L'elemento** group definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.

## <a name="attributes"></a>Attributi

[**bitdepth**](bitdepth-attribute.md), [**buffering,**](buffering-attribute.md) [**framerate**](framerate-attribute.md), [**height**](height-attribute.md) [**,**](lock-attribute.md)lock , [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|----------------------------------------------------------------------------------------------------------|
| Padre   | [**linea temporale**](timeline-element.md)                                                                     |
| Children | [**composito,**](composite-element.md) [**effetto,**](effect-element.md) [**traccia**](track-element.md) |



 

## <a name="remarks"></a>Commenti

`group`All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito dall'ordine in cui appaiono all'interno dell'elemento. Il primo livello ha la priorità 0 e i livelli successivi hanno valori di priorità crescenti.

## <a name="examples"></a>Esempi


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



