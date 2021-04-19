---
title: Controls. fastReverse, metodo
description: Il metodo fastReverse avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Metodo fastReverse Windows Media Player
- Metodo fastReverse Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo fastReverse
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
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327071"
---
# <a name="controlsfastreverse-method"></a>Controls. fastReverse, metodo

Il metodo **fastReverse** avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.

## <a name="syntax"></a>Sintassi


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **fastReverse** analizza il clip in senso inverso cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video. La chiamata di **fastReverse** modifica le *Impostazioni*. proprietà **rate** su 5,0. Se la **frequenza** viene modificata in seguito o se viene chiamato il metodo **Play** o **Stop** , Windows Media Player interromperà velocemente.

Se l'elemento fa parte di una playlist, **fastReverse** si interrompe all'inizio della traccia corrente. Ad esempio, se Track 3 si trova in **fastReverse**, quando si raggiunge l'inizio di Track 3, Windows Media Player non passerà a Track 2. Il numero di Play non viene incrementato quando si chiama **fastReverse**.

Se si chiama **fastForward** mentre **fastReverse** è attivo, **fastReverse** verrà arrestato e **fastForward** inizierà.

Questo metodo non funziona per le trasmissioni live e per determinati tipi di supporti. Per determinare se è possibile utilizzare l'inversione veloce in un clip **, chiamare il** campo ("FastReverse").

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **fastReverse** per avviare la riproduzione veloce dell'elemento multimediale. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. disavailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





