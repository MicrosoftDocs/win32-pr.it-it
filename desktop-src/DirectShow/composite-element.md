---
description: L'elemento composito definisce una composizione, un oggetto contenitore per tracce e altre composizione annidate.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908839"
---
# <a name="composite-element"></a>Elemento composite

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`composite`L'elemento definisce una composizione, un oggetto contenitore per tracce e altre composizione annidate.

## <a name="attributes"></a>Attributi

[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Padre   | `composite`, [ **group**](group-element.md)                                                                             |
| Children | `composite`, [**effetto**](effect-element.md), [**traccia**](track-element.md), [**transizione**](transition-element.md) |



 

## <a name="remarks"></a>Commenti

`composite`All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito dall'ordine in cui vengono visualizzati all'interno dell'elemento. Il primo livello ha la priorità 0 e i livelli successivi hanno valori di priorità crescenti.

## <a name="examples"></a>Esempi


```XML
<composite> </composite>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



