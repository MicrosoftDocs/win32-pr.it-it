---
title: BUTTONELEMENT.sticky
description: L'attributo sticky specifica o recupera un valore che indica se BUTTONELEMENT è un interruttore, ad esempio se si tratta di un pulsante a due stati o a stato singolo.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT.sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8a709fc28f0d1529c58725db5856931195a66cc370559dd9d14af61e869db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120038"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT.sticky

**L'attributo sticky** specifica o recupera un valore che indica se **BUTTONELEMENT** è un interruttore, ad esempio se si tratta di un pulsante a due stati o a stato singolo.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** è di tipo sticky.              |
| false | Valore predefinito. **BUTTONELEMENT** non è di tipo sticky. |



 

## <a name="remarks"></a>Commenti

Se **l'attributo sticky** è impostato su true, l'elemento pulsante verrà impostato sullo stato down quando viene selezionato e rimarrà in tale stato fino a quando non viene nuovamente selezionato. Quando l'elemento pulsante è in stato down, l'attributo **down** sarà true e verrà visualizzata la parte appropriata del gruppo di pulsanti **downImage.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





