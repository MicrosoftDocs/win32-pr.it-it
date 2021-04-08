---
description: L'elemento at definisce il valore di un elemento param in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene il parametro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747263"
---
# <a name="at-element"></a>Elemento at

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `at` elemento definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene il parametro. L' `at` elemento causa il passaggio improvviso del parametro al nuovo valore nel momento specificato. Per una progressione uniforme a un nuovo valore, usare l'elemento [**lineare**](linear-element.md) .

## <a name="attributes"></a>Attributi

[**ora**](time-attribute.md), [ **valore**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                |
|----------|--------------------------------|
| Padre   | [**param**](param-element.md) |
| Children | nessuno                           |



 

## <a name="examples"></a>Esempi


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



