---
title: Comando MCI_PAUSE (mmsystem. h)
description: Il \_ comando di sospensione MCI sospende l'azione corrente. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- Comando MCI_PAUSE Windows Multimedia
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
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739823"
---
# <a name="mci_pause-command"></a>\_Comando di sospensione MCI

Il \_ comando di sospensione MCI sospende l'azione corrente. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La differenza tra i comandi [MCI \_ Stop](mci-stop.md) e MCI \_ pause dipende dal dispositivo. Se possibile, \_ la sospensione MCI sospende l'operazione del dispositivo, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione. Con i driver MCICDA, MCISEQ e MCIPIONR, il comando MCI \_ pause funziona allo stesso modo del comando MCI \_ stop.

Per i dispositivi digitali video, il parametro *lpPause* punta a una struttura [**DGV di \_ \_ sospensione \_ parametri MCI**](/previous-versions//dd743395(v=vs.85)) .

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

 

