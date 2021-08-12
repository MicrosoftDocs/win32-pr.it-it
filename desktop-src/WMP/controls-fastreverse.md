---
title: Metodo Controls.fastReverse
description: Il metodo fastReverse avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Metodo fastReverse Windows Media Player
- Metodo fastReverse Windows Media Player , classe Controls
- Classe Controls Windows Media Player, metodo fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4643525f66102cbd7b017a4a48f1068489062ec0849f197f1f55df45fc6f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580277"
---
# <a name="controlsfastreverse-method"></a>Metodo Controls.fastReverse

Il **metodo fastReverse** avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.

## <a name="syntax"></a>Sintassi


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo fastReverse** analizza il clip in senso inverso a cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video. La chiamata **di fastReverse** modifica il *Impostazioni*. **impostare** la proprietà rate su 5.0. Se **la frequenza** viene successivamente modificata o se viene **chiamato play** o **stop,** Windows Media Player verrà interrotta l'inversione rapida.

Se l'elemento fa parte di una playlist, **fastReverse** si arresta all'inizio della traccia corrente. Ad esempio, se la traccia 3 è in **fastReverse**, quando viene raggiunta l'inizio della traccia 3, Windows Media Player non andrà alla traccia 2. Il conteggio di riproduzione non viene incrementato quando si chiama **fastReverse**.

Se si chiama **fastForward** mentre **fastReverse** è attivo, **fastReverse** verrà arrestato e **fastForward** inizierà.

Questo metodo non funziona per le trasmissioni live e alcuni tipi di supporti. Per determinare se è possibile usare fast reverse in un clip, chiamare **isAvailable**("FastReverse").

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **fastReverse** per avviare la riproduzione inversa rapida dell'elemento multimediale. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
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

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Impostazioni.rate**](settings-rate.md)
</dt> </dl>

 

 





