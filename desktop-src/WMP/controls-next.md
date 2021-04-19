---
title: Controls. Next (metodo)
description: Il metodo successivo imposta l'elemento corrente sull'elemento successivo nella playlist.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- Metodo Next Windows Media Player
- Metodo Next Windows Media Player, classe Controls
- Controlla la classe Windows Media Player, metodo successivo
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
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333424"
---
# <a name="controlsnext-method"></a>Controls. Next (metodo)

Il metodo **successivo** imposta l'elemento corrente sull'elemento successivo nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Controls.next()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la playlist si trova nell'ultima voce alla chiamata **successiva** , la prima voce nella playlist diventerà quella corrente.

Per le playlist lato server, questo metodo passa all'elemento successivo nella playlist sul lato server, non nella playlist del client.

Quando si riproduce un DVD, questo metodo passa al capitolo logico successivo nella sequenza di riproduzione, che potrebbe non essere il capitolo successivo nella playlist. Quando si giocano ancora i DVD, questo metodo passa alla successiva.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **Next** per passare all'elemento successivo nella playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controlli. Previous**](controls-previous.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





