---
title: CUSTOMSLIDER. Value
description: L'attributo value specifica o recupera la posizione corrente del dispositivo di scorrimento. | CUSTOMSLIDER. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- Media Player di Windows CUSTOMSLIDER. Value
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331747"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER. Value

L'attributo **value** specifica o recupera la posizione corrente del dispositivo di scorrimento.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore predefinito uguale all'attributo **min** .

## <a name="remarks"></a>Commenti

Il **valore** deve essere maggiore o uguale a **min** e minore o uguale a **Max**. Se il valore non rientra nell'intervallo, viene generato un avviso e il valore non viene modificato.

## <a name="examples"></a>Esempio

Vedere l'attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **CUSTOMSLIDER** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





