---
description: L'elemento transition definisce un oggetto transition. Una transizione è una trasformazione a due input che comporta una transizione da un flusso (ad esempio una composita o una traccia) a un altro.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910039"
---
# <a name="transition-element"></a>Elemento transition

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`transition`L'elemento definisce un oggetto di transizione. Una transizione è una trasformazione a due input che comporta una transizione da un flusso (ad esempio una composita o una traccia) a un altro.

## <a name="attributes"></a>Attributi

[**clsid**](clsid-attribute.md), cutpoint , [**cutpoint**](cutpoint-attribute.md) [**,**](lock-attribute.md) [**cutonly**](cutsonly-attribute.md), lock , [**mute**](mute-attribute.md), start , [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md) [](start-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|------------------------------------------------------------------------|
| Padre   | [**composito,**](composite-element.md) [ **traccia**](track-element.md) |
| Children | [**Param**](param-element.md)                                         |



 

## <a name="remarks"></a>Commenti

**L'attributo clsid** specifica il sottooggetto che crea la transizione.

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

 

 



