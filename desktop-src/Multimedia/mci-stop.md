---
title: Comando MCI_STOP (mmsystem. h)
description: Il \_ comando MCI stop arresta tutte le sequenze di riproduzione e di record, Scarica tutti i buffer di riproduzione e interrompe la visualizzazione delle immagini video. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Comando MCI_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400679"
---
# <a name="mci_stop-command"></a>\_Comando di arresto MCI

Il \_ comando MCI stop arresta tutte le sequenze di riproduzione e di record, Scarica tutti i buffer di riproduzione e interrompe la visualizzazione delle immagini video. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La differenza tra i \_ comandi MCI stop e [MCI \_ pause](mci-pause.md) dipende dal dispositivo. Se possibile, \_ la sospensione MCI sospende l'operazione del dispositivo, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione.

Per il dispositivo audio CD, MCI \_ Stop Reimposta la posizione di rilevamento corrente su zero. al contrario, [MCI \_ pause](mci-pause.md) mantiene la posizione corrente, prevedendo che il dispositivo riprende la riproduzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

