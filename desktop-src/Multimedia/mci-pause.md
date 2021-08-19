---
title: MCI_PAUSE comando (Mmsystem.h)
description: Il comando MCI \_ PAUSE sospende l'azione corrente. Questo comando viene riconosciuto da dispositivi cd audio, digital-video, MIDI Sequencer, VCR, videodisc e waveform-audio.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2318a10e7b03bf89d616bd6ff2373cdf785b0bb4015ab4b308ead57d7f9223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803499"
---
# <a name="mci_pause-command"></a>Comando MCI \_ PAUSE

Il comando MCI \_ PAUSE sospende l'azione corrente. Questo comando viene riconosciuto da dispositivi cd audio, digital-video, MIDI Sequencer, VCR, videodisc e waveform-audio.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT o, per i dispositivi video digitale e \_ VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*
</dt> <dd>

Puntatore a una [**struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La differenza tra [i comandi MCI \_ STOP](mci-stop.md) e MCI \_ PAUSE dipende dal dispositivo. Se possibile, MCI \_ PAUSE sospende il funzionamento del dispositivo, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione. Con i driver MCICDA, MCISEQ e MCIPIONR, il comando MCI PAUSE funziona come \_ il comando MCI \_ STOP.

Per i dispositivi video digitali, il *parametro lpPause* punta a una [**struttura MCI \_ DGV \_ PAUSE \_ PARMS.**](/previous-versions//dd743395(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

