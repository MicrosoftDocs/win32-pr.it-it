---
title: Sospendi comando
description: Il comando Sospendi sospende la riproduzione o la registrazione.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- Sospendi comando Windows Multimedia
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874622"
---
# <a name="pause-command"></a>Sospendi comando

Il comando Sospendi sospende la riproduzione o la registrazione. La maggior parte dei driver mantiene la posizione corrente e, infine, riprende la riproduzione o la registrazione in questa posizione. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con i driver MCICDA, MCISEQ e MCIPIONR, il comando pause funziona allo stesso modo del comando [Stop](stop.md) .

## <a name="examples"></a>Esempio

Il comando che segue sospende il dispositivo "audio".

``` syntax
pause mysound
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
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

