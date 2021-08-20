---
description: L'elemento at definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824391"
---
# <a name="at-element"></a>Elemento at

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'elemento definisce il valore di un elemento `at` [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro . L'elemento fa sì che il parametro salti improvvisamente `at` al nuovo valore all'ora specificata. Per una progressione uniforme a un nuovo valore, usare [**l'elemento lineare.**](linear-element.md)

## <a name="attributes"></a>Attributi

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|--------------------------------|
| Padre   | [**Param**](param-element.md) |
| Children | Nessuno                           |



 

## <a name="examples"></a>Esempi


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



