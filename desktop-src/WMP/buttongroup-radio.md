---
title: BUTTONGROUP. radio
description: L'attributo radio specifica o recupera un valore che indica se BUTTONGROUP è costituito da pulsanti di opzione.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- Media Player BUTTONGROUP. Radio Windows
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330254"
---
# <a name="buttongroupradio"></a>BUTTONGROUP. radio

L'attributo **Radio** specifica o recupera un valore che indica se **ButtonGroup** è costituito da pulsanti di opzione.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                      |
|-------|--------------------------------------------------|
| true  | **ButtonGroup** è uno stile radio.              |
| false | Valore predefinito. Il **ButtonGroup** non è di tipo radio. |



 

## <a name="remarks"></a>Commenti

Se **Radio** è impostato su true, tutti gli elementi **ButtonElement** in **ButtonGroup** saranno permanenti, ma solo un pulsante alla volta sarà nello stato di inattività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONelement. Sticky**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





