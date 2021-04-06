---
title: Comando MCI_RESUME (mmsystem. h)
description: Il \_ comando MCI Resume causa il riavvio dell'operazione sospesa da parte di un dispositivo in pausa.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- Comando MCI_RESUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963878"
---
# <a name="mci_resume-command"></a>\_Comando MCI Resume

Il \_ comando MCI Resume causa il riavvio dell'operazione sospesa da parte di un dispositivo in pausa. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando. Anche se i dispositivi CD audio, MIDI sequencer e videodisco riconoscono questo comando, i driver di dispositivo MCICDA, MCISEQ e MCIPIONR non lo supportano.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
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

<span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando riprende la riproduzione e la registrazione senza modificare il set di posizioni della traccia corrente con [il \_ record](mci-record.md) [MCI \_ Play](mci-play.md) o MCI.

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

 

