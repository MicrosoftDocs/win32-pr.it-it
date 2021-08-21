---
title: BUTTON.sticky
description: L'attributo sticky specifica o recupera un valore che indica se BUTTON è un interruttore, ad esempio se si tratta di un pulsante a due stati o a stato singolo.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON.sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9c6a2cf1523cf2384142bd6ffd47cb5e42e7851dc96b6e236343c5ba670aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342747"
---
# <a name="buttonsticky"></a>BUTTON.sticky

**L'attributo sticky** specifica o recupera un valore che indica se **BUTTON** è un interruttore, ad esempio se si tratta di un PULSANTE a due stati o a stato **singolo.**

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                        |
|-------|------------------------------------|
| true  | **BUTTON** è di tipo sticky.              |
| false | Valore predefinito. **BUTTON** non è sticky. |



 

## <a name="remarks"></a>Commenti

Se **sticky è** impostato su true, il **PULSANTE** verrà impostato sullo stato down quando si fa clic su e rimarrà in tale stato fino a quando non si fa di nuovo clic. Quando button **è** in stato down, l'attributo **down** sarà true e verrà visualizzato **downImage.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





