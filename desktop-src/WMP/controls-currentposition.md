---
title: Controls.currentPosition
description: La proprietà currentPosition specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls.currentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be64d23b65a396cfb15e9f7b19b4571bdb26cbb7f308241e9a381375b9d26a40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341878"
---
# <a name="controlscurrentposition"></a>Controls.currentPosition

La **proprietà currentPosition** specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**double**).

## <a name="examples"></a>Esempio

L'esempio seguente usa **currentPosition** per cercare una posizione fornita dall'utente. Viene creato un elemento BUTTON HTML per eseguire il JScript codice. È stato creato un elemento di input HTML TEXT denominato setPosition per accettare un valore, espresso in secondi, dall'utente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





