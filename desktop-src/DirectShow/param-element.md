---
description: L'elemento param specifica il valore di una proprietà su una transizione, un effetto o un altro oggetto secondario.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35c58543c5daae7ad0a77f6380bc3f3db48cf8443461eaf919c4c727163436cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050821"
---
# <a name="param-element"></a>Elemento param

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`param`L'elemento specifica il valore di una proprietà su una transizione, un effetto o un altro oggetto secondario.

## <a name="attributes"></a>Attributi

[**name**](name-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|----------------------------------------------------------------------------------------------------------|
| Padre   | [**clip,**](clip-element.md) [**effetto,**](effect-element.md) [**transizione**](transition-element.md) |
| Children | [**in**](at-element.md), [ **lineare**](linear-element.md)                                               |



 

## <a name="remarks"></a>Commenti

**L'attributo** value specifica il valore della proprietà all'inizio della transizione o dell'effetto. Usare **l'elemento at** o **linear** per specificare la modifica dei valori. Se **l'elemento param** non contiene **elementi at** o **lineari,** il valore rimane costante per la durata dell'effetto o della transizione.

> [!Note]  
> Un **elemento param all'interno** di **un elemento clip** non può **contenere elementi at** o **lineari.**

 

Molte transizioni supportano una proprietà **Progress** standard che varia da 0 a 1,0, che indica la percentuale della transizione riflessa nell'output. In **Progress** = 0.0 la transizione si trova all'inizio della sequenza (interamente la prima immagine video). In **Progress** = 0,5 la transizione è metà completa. (Ad esempio, in una cancellazione, in **Progress** = 0,5 il limite di transizione si trova al centro dell'immagine) In **Progress** = 1.0 la transizione è completa (interamente la seconda immagine). Per impostazione predefinita, le transizioni passano da **Progress** = 0.0 all'inizio della transizione **a Progress** = 1.0 alla fine.

Altre proprietà sono in genere specifiche di una particolare transizione o effetto. Ad esempio, la transizione di cancellazione supporta una **proprietà GradientSize** che controlla la larghezza dell'area di transizione.

Per eseguire una transizione all'indietro, impostare la proprietà **Progress** su 1.0 all'inizio della transizione e usare l'elemento **lineare** per impostare il valore su 0,0, come illustrato nell'esempio seguente:


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>Esempi


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



