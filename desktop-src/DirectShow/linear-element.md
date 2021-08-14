---
description: L'elemento lineare definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene l'elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34bff0ef1ef4c9c95752f986aabeddd24b40cc695a8a0f292b1072dfdc1d3d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397145"
---
# <a name="linear-element"></a>Elemento linear

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'elemento lineare definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene **l'elemento param.** `linear`L'elemento fa sì che il parametro esere una transizione uniforme dal valore precedente al nuovo valore. Per un passaggio istantaneo a un nuovo valore, usare [**l'elemento at.**](at-element.md)

## <a name="attributes"></a>Attributi

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|--------------------------------|
| Padre   | [**Param**](param-element.md) |
| Children | Nessuno                           |



 

## <a name="examples"></a>Esempio


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Camerauicontrol.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 




