---
description: L'elemento group definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda120363540eaf467ebb9beaea4705c4b430077c55b5b05c46197d90920b40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997831"
---
# <a name="group-element"></a>Elemento group

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

**L'elemento group** definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.

## <a name="attributes"></a>Attributi

[**bitdepth,**](bitdepth-attribute.md) [**buffering,**](buffering-attribute.md) [**framerate,**](framerate-attribute.md) [**height,**](height-attribute.md) [**lock,**](lock-attribute.md) [**mute,**](mute-attribute.md) [**name,**](name-attribute.md) [**previewmode,**](previewmode-attribute.md) [**samplingrate,**](samplingrate-attribute.md) [**type,**](type-attribute.md) [**userdata,**](userdata-attribute.md) [**userid,**](userid-attribute.md) [**username,**](username-attribute.md) [**width**](width-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|----------------------------------------------------------------------------------------------------------|
| Padre   | [**linea temporale**](timeline-element.md)                                                                     |
| Children | [**composite,**](composite-element.md) [**effect,**](effect-element.md) [**track**](track-element.md) |



 

## <a name="remarks"></a>Commenti

All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito in `group` base all'ordine in cui vengono visualizzati all'interno dell'elemento. Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità crescenti.

## <a name="examples"></a>Esempi


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



