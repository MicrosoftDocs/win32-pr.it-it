---
title: BUTTON. Sticky
description: L'attributo Sticky specifica o recupera un valore che indica se il pulsante è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON. Sticky Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325261"
---
# <a name="buttonsticky"></a>BUTTON. Sticky

L'attributo **Sticky** specifica o recupera un valore che indica se il **pulsante** è un interruttore, ovvero se si tratta di un **pulsante** a due Stati o di uno stato singolo.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                        |
|-------|------------------------------------|
| true  | Il **pulsante** è appiccicoso.              |
| false | Valore predefinito. Il **pulsante** non è appiccicoso. |



 

## <a name="remarks"></a>Commenti

Se **Sticky** è impostato su true, il **pulsante** passerà allo stato inattivo quando si fa clic e rimarrà in tale stato fino a quando non si fa clic di nuovo su. Quando il **pulsante** è nello stato di inattività, l'attributo **Down** sarà true e verrà visualizzato **downImage** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**PULSANTE in basso**](button-down.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





