---
title: MCI_STOP comando (Mmsystem.h)
description: Il comando MCI STOP arresta tutte le sequenze di riproduzione e registrazione, scarica tutti i buffer di riproduzione e interrompe \_ la visualizzazione delle immagini video. Questo comando viene riconosciuto da cd audio, digital-video, sequencer MIDI, videodisc, videoregistratore e dispositivi audio waveform.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP comando Windows Multimedia
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
ms.openlocfilehash: e02830dde544e025447cb72df6ff3720857985384ff6bd074c5e0718b114697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374603"
---
# <a name="mci_stop-command"></a>Comando MCI \_ STOP

Il comando MCI STOP arresta tutte le sequenze di riproduzione e registrazione, scarica tutti i buffer di riproduzione e interrompe \_ la visualizzazione delle immagini video. Questo comando viene riconosciuto da cd audio, digital-video, sequencer MIDI, videodisc, videoregistratore e dispositivi audio waveform.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La differenza tra i comandi MCI \_ STOP [e MCI \_ PAUSE](mci-pause.md) dipende dal dispositivo. Se possibile, MCI \_ PAUSE sospende il funzionamento del dispositivo ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione.

Per il dispositivo audio CD, MCI STOP reimposta la posizione della traccia corrente su zero. AL \_ contrario, [MCI \_ PAUSE](mci-pause.md) mantiene la posizione corrente della traccia, anticipando la ripresa della riproduzione del dispositivo.

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

 

