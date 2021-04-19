---
title: Controls. currentPosition
description: La proprietà currentPosition specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Media Player di Windows Controls. currentPosition
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
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331762"
---
# <a name="controlscurrentposition"></a>Controls. currentPosition

La proprietà **currentPosition** specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Double**).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **currentPosition** per cercare una posizione fornita dall'utente. Viene creato un elemento BUTTON HTML per eseguire il codice JScript. È stato creato un elemento input di testo HTML, denominato seposition, per accettare un valore, in secondi, dall'utente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





