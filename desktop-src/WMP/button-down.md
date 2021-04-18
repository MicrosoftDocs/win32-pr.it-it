---
title: PULSANTE in basso
description: L'attributo Down specifica o recupera un valore che indica se il pulsante si trova nella posizione verso l'alto o verso il basso.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BUTTON. Down Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328893"
---
# <a name="buttondown"></a>PULSANTE in basso

L'attributo **Down** specifica o recupera un valore che indica se il **pulsante** si trova nella posizione verso l'alto o verso il basso.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                   |
|-------|---------------------------------------------------------------|
| true  | Indica che il **pulsante** si trova nella posizione in giù.        |
| false | Valore predefinito. Indica che il **pulsante** si trova nella posizione verso l'alto. |



 

## <a name="remarks"></a>Commenti

Affinché un **pulsante** rimanga nella posizione in giù, **Sticky** deve essere impostato su true. Per impostazione predefinita, **Sticky** è false e qualsiasi tentativo **di impostare il valore su** true verrà ignorato.

Se viene specificato un valore non valido, viene mantenuto lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON. downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





