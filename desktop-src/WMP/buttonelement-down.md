---
title: BUTTONelement. Down
description: L'attributo Down specifica o recupera un valore che indica se l'elemento Button si trova nella posizione verso l'alto o verso il basso.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONelement. Down Media Player di Windows
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329087"
---
# <a name="buttonelementdown"></a>BUTTONelement. Down

L'attributo **Down** specifica o recupera un valore che indica se l'elemento Button si trova nella posizione verso l'alto o verso il basso.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica che il **pulsante** è nella posizione in giù.        |
| false | Valore predefinito. Indica che il **pulsante** è nella posizione verso l'alto. |



 

## <a name="remarks"></a>Commenti

Affinché un elemento Button rimanga nella posizione in giù, **Sticky** deve essere impostato su true. Per impostazione predefinita, **Sticky** è false e qualsiasi tentativo **di impostare il valore su** true verrà ignorato.

Se viene specificato un valore non valido, viene mantenuto lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONelement (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONelement. downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





