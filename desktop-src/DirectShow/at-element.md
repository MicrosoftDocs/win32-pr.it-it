---
description: L'elemento at definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909829"
---
# <a name="at-element"></a>Elemento at

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'elemento definisce il valore di un elemento `at` [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro . L'elemento fa sì che il parametro salti improvvisamente `at` al nuovo valore all'ora specificata. Per una progressione uniforme a un nuovo valore, usare [**l'elemento lineare.**](linear-element.md)

## <a name="attributes"></a>Attributi

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|--------------------------------|
| Padre   | [**Param**](param-element.md) |
| Children | nessuno                           |



 

## <a name="examples"></a>Esempi


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



