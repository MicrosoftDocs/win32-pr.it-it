---
title: comando stop
description: Il comando stop arresta la riproduzione o la registrazione. I dispositivi audio CD, digital-video, MIDI Sequencer, videodisc, VCR e audio waveform riconoscono questo comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Comando stop Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3091fcf3c58dc015450a9d585af48cc8347d4167bdd487c37dd3f7c6cd4f04e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037111"
---
# <a name="stop-command"></a>comando stop

Il comando stop arresta la riproduzione o la registrazione. I dispositivi audio CD, digital-video, MIDI Sequencer, videodisc, VCR e audio waveform riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*
</dt> <dd>

Per i dispositivi video digitali, può essere il flag seguente.



| Valore | Significato                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tenere  | Impedisce il rilascio delle risorse necessarie per ridisegnare un'immagine ancorata sullo schermo. Il buffer dei frame rimane disponibile per l'aggiornamento della visualizzazione quando, ad esempio, la finestra viene spostata. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Per i dispositivi audio CD, il comando stop arresta la riproduzione e reimposta la posizione della traccia corrente su zero.

## <a name="examples"></a>Esempio

Il comando seguente arresta la riproduzione o la registrazione nel dispositivo "mysound".

``` syntax
stop mysound
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

