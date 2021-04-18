---
title: BUTTONelement. Sticky
description: L'attributo Sticky specifica o recupera un valore che indica se BUTTONelement è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONelement. Sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329205"
---
# <a name="buttonelementsticky"></a>BUTTONelement. Sticky

L'attributo **Sticky** specifica o recupera un valore che indica se **ButtonElement** è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                               |
|-------|-------------------------------------------|
| true  | **ButtonElement** è appiccicoso.              |
| false | Valore predefinito. **ButtonElement** non è appiccicoso. |



 

## <a name="remarks"></a>Commenti

Se l'attributo **Sticky** è impostato su true, l'elemento Button passerà allo stato inattivo quando si fa clic su di esso e rimarrà in tale stato fino a quando non si fa clic di nuovo su. Quando l'elemento Button si trova nello stato inattivo, l'attributo **Down** sarà true e verrà visualizzata la parte appropriata del gruppo di pulsanti **downImage** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONelement (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONelement. Down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





