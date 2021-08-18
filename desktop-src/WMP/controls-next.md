---
title: Metodo Controls.next
description: Il metodo next imposta l'elemento corrente sull'elemento successivo nella playlist.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- Metodo next Windows Media Player
- Metodo next Windows Media Player , classe Controls
- Classe Controls Windows Media Player , metodo next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997471"
---
# <a name="controlsnext-method"></a>Metodo Controls.next

Il **metodo** next imposta l'elemento corrente sull'elemento successivo nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Controls.next()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la playlist si trova nell'ultima voce quando viene richiamato **next,** la prima voce nella playlist diventerà quella corrente.

Per le playlist sul lato server, questo metodo passa all'elemento successivo nella playlist sul lato server, non alla playlist client.

Quando si riproduce un DVD, questo metodo passa al capitolo logico successivo nella sequenza di riproduzione, che potrebbe non essere il capitolo successivo della playlist. Quando si riproduce ancora un DVD, questo metodo passa al successivo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **next** per passare all'elemento successivo nella playlist corrente. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
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
</dt> <dt>

[**Controls.previous**](controls-previous.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 





