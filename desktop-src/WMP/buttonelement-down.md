---
title: BUTTONELEMENT.down
description: L'attributo down specifica o recupera un valore che indica se l'elemento pulsante si trova nella posizione verso l'alto o verso il basso.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT.down Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff20aebda01b24dc14eb7d5298ee0d663d903bedcb7ef6ef8b05b6211af8b567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764471"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT.down

**L'attributo** down specifica o recupera un valore che indica se l'elemento pulsante si trova nella posizione verso l'alto o verso il basso.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica che **BUTTONELEMENT** si trova nella posizione verso il basso.        |
| false | Valore predefinito. Indica che **BUTTONELEMENT** si trova nella posizione verso l'alto. |



 

## <a name="remarks"></a>Commenti

Per mantenere un elemento pulsante nella posizione verso il basso, **sticky** deve essere impostato su true. Per impostazione predefinita, **sticky** è false e qualsiasi tentativo di impostare **su** true verrà ignorato.

Se viene specificato un valore non valido, viene mantenuto lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





