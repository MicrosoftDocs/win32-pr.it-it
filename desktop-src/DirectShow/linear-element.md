---
description: L'elemento lineare definisce il valore di un elemento param in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene l'elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento Linear (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324786"
---
# <a name="linear-element"></a>Elemento lineare

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'elemento lineare definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene l'elemento **param** . L' `linear` elemento fa in modo che il parametro effettui una transizione uniforme dal valore precedente al nuovo valore. Per passare immediatamente a un nuovo valore, usare l'elemento [**at**](at-element.md) .

## <a name="attributes"></a>Attributi

[**ora**](time-attribute.md), [ **valore**](value-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                |
|----------|--------------------------------|
| Padre   | [**param**](param-element.md) |
| Children | nessuno                           |



 

## <a name="examples"></a>Esempio


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 




