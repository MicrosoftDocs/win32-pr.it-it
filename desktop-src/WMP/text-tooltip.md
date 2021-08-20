---
title: TEXT.toolTip
description: L'attributo toolTip specifica o recupera il testo della descrizione comando per il controllo di testo.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- Text.toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 726337ffb31b86d4eaa3a20a1d922fc622110b647fe9be747e8ae239c4548276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831820"
---
# <a name="texttooltip"></a>TEXT.toolTip

**L'attributo toolTip** specifica o recupera il testo della descrizione comando per il controllo di testo.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa **di** lettura/scrittura con una lunghezza massima di 1024 caratteri. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se questo attributo non è specificato  e il testo nell'attributo value viene troncato nel controllo Text o **wordWrap** è impostato su true, nella descrizione comando verrà visualizzato il testo completo dell'attributo **value.**

Quando questo attributo è impostato su "" (stringa vuota), non viene visualizzata alcuna descrizione comando.

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati **gli** attributi dell'elemento TEXT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





