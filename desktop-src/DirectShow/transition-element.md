---
description: L'elemento Transition definisce un oggetto di transizione. Una transizione è una trasformazione di due input che consente di eseguire una transizione da un flusso a un altro (ad esempio un composto o una traccia).
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Transition (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313408"
---
# <a name="transition-element"></a>Transition (elemento)

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `transition` elemento definisce un oggetto di transizione. Una transizione è una trasformazione di due input che consente di eseguire una transizione da un flusso a un altro (ad esempio un composto o una traccia).

## <a name="attributes"></a>Attributi

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| Padre   | [**composto**](composite-element.md), [ **traccia**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Commenti

L'attributo **CLSID** specifica il sottooggetto che crea la transizione.

## <a name="examples"></a>Esempi


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



