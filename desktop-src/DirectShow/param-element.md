---
description: L'elemento param Specifica il valore di una proprietà in una transizione, un effetto o un altro oggetto SubObject.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876786"
---
# <a name="param-element"></a>param (elemento)

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `param` elemento specifica il valore di una proprietà in una transizione, un effetto o un altro oggetto SubObject.

## <a name="attributes"></a>Attributi

[**nome**](name-attribute.md), [ **valore**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Padre   | [**clip**](clip-element.md), [**effetto**](effect-element.md), [**transizione**](transition-element.md) |
| Children | [**at**](at-element.md), [ **lineari**](linear-element.md)                                               |



 

## <a name="remarks"></a>Commenti

L'attributo **value** specifica il valore della proprietà all'inizio della transizione o dell'effetto. Usare l'elemento **at** o **Linear** per specificare i valori modificabili. Se l'elemento **param** non contiene elementi **at** o **Linear** , il valore rimane costante per la durata dell'effetto o della transizione.

> [!Note]  
> Un elemento **param** all'interno di un elemento **clip** non può contenere elementi **at** o **Linear** .

 

Molte transizioni supportano una proprietà dello **stato di avanzamento** standard compresa tra 0 e 1,0, che indica la percentuale della transizione che si riflette nell'output. In fase di **esecuzione** = 0,0, la transizione si trova all'inizio della relativa sequenza (interamente la prima immagine video). In fase di **esecuzione** = 0,5, la transizione è metà del completamento. (Ad esempio, in una cancellazione, in **corso** = 0,5 il limite di transizione è al centro dell'immagine) In fase di **esecuzione** = 1,0, la transizione è completa (interamente la seconda immagine). Per impostazione predefinita, le transizioni passano da **Progress** = 0,0 all'inizio della transizione a **Progress** = 1,0 alla fine.

Le altre proprietà sono in genere specifiche di una particolare transizione o effetto. Ad esempio, la transizione di cancellazione supporta una proprietà **GradientSize** che controlla la larghezza dell'area di transizione.

Per eseguire una transizione indietro, impostare la proprietà **Progress** su 1,0 all'inizio della transizione e usare l'elemento **Linear** per modificare il valore in 0,0, come illustrato nell'esempio seguente:


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

 

 



