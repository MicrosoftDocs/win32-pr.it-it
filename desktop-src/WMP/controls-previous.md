---
title: Controls. Previous, metodo
description: Il metodo precedente imposta l'elemento corrente sull'elemento precedente nella playlist.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- Metodo precedente Media Player Windows
- Metodo precedente Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo precedente
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330003"
---
# <a name="controlsprevious-method"></a>Controls. Previous, metodo

Il metodo **precedente** imposta l'elemento corrente sull'elemento precedente nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la playlist si trova nella prima voce quando viene richiamato il **precedente** , l'ultima voce nella playlist diventerà quella corrente.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **Previous** per passare all'elemento precedente nella playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
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

[**Controlli. Next**](controls-next.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





