---
title: Controls. fastForward, metodo
description: Il metodo fastForward avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti. | Controls. fastForward, metodo
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Metodo fastForward Windows Media Player
- Metodo fastForward Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327072"
---
# <a name="controlsfastforward-method"></a>Controls. fastForward, metodo

Il metodo **fastForward** avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti.

## <a name="syntax"></a>Sintassi


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **fastForward** riproduce il ritaglio cinque volte la velocità normale. La chiamata di **fastForward** modifica le *Impostazioni*. proprietà **rate** su 5,0. Se la **frequenza** viene modificata o se viene chiamato il metodo **Play** o **Stop** , Windows Media Player interromperà l'invio rapido.

Il metodo **fastForward** non funziona per le trasmissioni live e per determinati tipi di supporti. Per determinare se è possibile eseguire l'avanzamento rapido in un clip, chiamare l'oggetto non **disponibile**("fastforward").

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **fastForward** per avviare la riproduzione rapida dell'elemento multimediale. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
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

[**Controls. disavailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





