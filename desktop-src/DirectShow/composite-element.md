---
description: L'elemento composito definisce una composizione, un oggetto contenitore per tracce e altre composizioni annidate.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084311"
---
# <a name="composite-element"></a>Elemento composite

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`composite`L'elemento definisce una composizione, un oggetto contenitore per tracce e altre composizioni annidate.

## <a name="attributes"></a>Attributi

[**lock,**](lock-attribute.md) [**mute,**](mute-attribute.md) [**userdata,**](userdata-attribute.md) [**userid,**](userid-attribute.md) [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Padre   | `composite`, [ **group**](group-element.md)                                                                             |
| Children | `composite`, [**effect,**](effect-element.md) [**track,**](track-element.md) [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Commenti

All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito in base `composite` all'ordine in cui vengono visualizzati all'interno dell'elemento. Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità crescenti.

## <a name="examples"></a>Esempi


```XML
<composite> </composite>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



