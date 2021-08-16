---
title: BUTTONGROUP.radio
description: L'attributo radio specifica o recupera un valore che indica se BUTTONGROUP è costituito da pulsanti di opzione.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP.radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997771"
---
# <a name="buttongroupradio"></a>BUTTONGROUP.radio

**L'attributo** radio specifica o recupera un valore che indica se **BUTTONGROUP** è costituito da pulsanti di opzione.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                      |
|-------|--------------------------------------------------|
| true  | BUTTONGROUP **è** uno stile di opzione.              |
| false | Valore predefinito. BUTTONGROUP **non** è uno stile di opzione. |



 

## <a name="remarks"></a>Commenti

Se **radio** è impostata su true, tutti gli elementi **BUTTONELEMENT** in **BUTTONGROUP** saranno appiccicosi, ma solo un pulsante alla volta sarà in stato down.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONELEMENT.sticky**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





