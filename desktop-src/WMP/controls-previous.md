---
title: Metodo Controls.previous
description: Il metodo precedente imposta l'elemento corrente sull'elemento precedente nella playlist.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- Metodo Windows Media Player
- Metodo previous Windows Media Player , classe Controls
- Classe Controls Windows Media Player , metodo precedente
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
ms.openlocfilehash: f67dbc80fb731f32eefb36f2a0f66c852da3da69dbc6b7ae56c03ebafb06e07e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119330"
---
# <a name="controlsprevious-method"></a>Metodo Controls.previous

Il **metodo** precedente imposta l'elemento corrente sull'elemento precedente nella playlist.

## <a name="syntax"></a>Sintassi


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la playlist si trova sulla prima voce quando **viene richiamato previous,** l'ultima voce nella playlist diventerà quella corrente.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **previous** per passare all'elemento precedente nella playlist corrente. **L'oggetto Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 





