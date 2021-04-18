---
description: L'elemento composito definisce una composizione, un oggetto contenitore per le tracce e altre composizioni nidificate.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303824"
---
# <a name="composite-element"></a>Elemento composite

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `composite` elemento definisce una composizione, un oggetto contenitore per le tracce e altre composizioni nidificate.

## <a name="attributes"></a>Attributi

[**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Padre   | `composite`, [ **gruppo**](group-element.md)                                                                             |
| Children | `composite`, [**effetto**](effect-element.md), [**traccia**](track-element.md), [**transizione**](transition-element.md) |



 

## <a name="remarks"></a>Commenti

All'interno di un `composite` elemento, la priorità dei livelli annidati viene determinata in modo implicito in base all'ordine in cui vengono visualizzati all'interno dell'elemento. Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità sempre maggiori.

## <a name="examples"></a>Esempi


```XML
<composite> </composite>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



