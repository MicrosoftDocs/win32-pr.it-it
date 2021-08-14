---
title: Metodo Controls.fastForward
description: Il metodo fastForward avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti. | Metodo Controls.fastForward
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Metodo fastForward Windows Media Player
- Metodo fastForward Windows Media Player , classe Controls
- Classe Controls Windows Media Player, metodo fastForward
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
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341817"
---
# <a name="controlsfastforward-method"></a>Metodo Controls.fastForward

Il **metodo fastForward** avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti.

## <a name="syntax"></a>Sintassi


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo fastForward** riproduce il clip a cinque volte la velocità normale. La chiamata **di fastForward** modifica il *Impostazioni*. **impostare** la proprietà rate su 5.0. Se **la frequenza** viene successivamente modificata o se viene **chiamato play** o **stop,** Windows Media Player l'inoltro rapido.

Il **metodo fastForward** non funziona per le trasmissioni live e alcuni tipi di supporti. Per determinare se è possibile procedere rapidamente in un clip, chiamare **isAvailable**("FastForward").

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **fastForward** per avviare la riproduzione veloce dell'elemento multimediale. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Impostazioni.rate**](settings-rate.md)
</dt> </dl>

 

 





