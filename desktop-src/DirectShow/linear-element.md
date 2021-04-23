---
description: L'elemento lineare definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene l'elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910089"
---
# <a name="linear-element"></a>Elemento linear

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'elemento lineare definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene **l'elemento param.** `linear`L'elemento fa sì che il parametro esere una transizione uniforme dal valore precedente al nuovo valore. Per un passaggio istantaneo a un nuovo valore, usare [**l'elemento at.**](at-element.md)

## <a name="attributes"></a>Attributi

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|--------------------------------|
| Padre   | [**Param**](param-element.md) |
| Children | nessuno                           |



 

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

 

 




