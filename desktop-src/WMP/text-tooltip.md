---
title: TESTO. toolTip
description: L'attributo toolTip specifica o Recupera il testo della descrizione comando per il controllo di testo.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TESTO. toolTip Media Player Windows
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327605"
---
# <a name="texttooltip"></a>TESTO. toolTip

L'attributo **ToolTip** specifica o Recupera il testo della descrizione comando per il controllo di testo.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura con una lunghezza massima di 1024 caratteri. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se questo attributo non viene specificato e il testo nell'attributo **value** viene troncato nel controllo testo, o **WordWrap** è impostato su true, la descrizione comando visualizzerà il testo completo dell'attributo **value** .

Quando questo attributo è impostato su "" (stringa vuota), non viene visualizzata alcuna descrizione comando.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> <dt>

[**TESTO. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





