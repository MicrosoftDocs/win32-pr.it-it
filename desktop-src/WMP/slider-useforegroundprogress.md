---
title: SLIDER. useForegroundProgress
description: L'attributo useForegroundProgress specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Media Player Windows SLIDER. useForegroundProgress
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325581"
---
# <a name="slideruseforegroundprogress"></a>SLIDER. useForegroundProgress

L'attributo **useForegroundProgress** specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| true  | USA stato in primo piano.                 |
| false | Valore predefinito. Non usare lo stato in primo piano. |



 

## <a name="remarks"></a>Commenti

Questo attributo consente di usare l'attributo **foregroundProgress** , che viene usato principalmente per tenere traccia dello stato di avanzamento del download di un file multimediale, monitorando contemporaneamente la posizione di riproduzione corrente del file usando l'attributo **value** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**SLIDER. Value**](slider-value.md)
</dt> </dl>

 

 





