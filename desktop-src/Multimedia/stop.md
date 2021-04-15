---
title: Interrompi comando
description: Il comando Stop interrompe la riproduzione o la registrazione. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Interrompi comando Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400615"
---
# <a name="stop-command"></a>Interrompi comando

Il comando Stop interrompe la riproduzione o la registrazione. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*
</dt> <dd>

Per i dispositivi digitali video, il flag può essere il seguente.



| Valore | Significato                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| contenere  | Impedisce il rilascio di risorse necessarie per ricreare un'immagine ancora sullo schermo. Il buffer del frame rimane disponibile per l'aggiornamento della visualizzazione quando, ad esempio, la finestra viene spostata. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per i dispositivi audio CD, il comando Interrompi arresta la riproduzione e reimposta la posizione corrente del rilevamento su zero.

## <a name="examples"></a>Esempio

Il comando seguente interrompe la riproduzione o la registrazione sul dispositivo "audio".

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

