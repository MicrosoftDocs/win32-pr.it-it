---
title: Comando MCI_DELETE (mmsystem. h)
description: Il \_ comando MCI Delete rimuove i dati dal file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Comando MCI_DELETE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964529"
---
# <a name="mci_delete-command"></a>\_Comando MCI Delete

Il \_ comando MCI Delete rimuove i dati dal file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag seguenti si applicano al tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>\_DGV \_ di MCI Delete \_
</dt> <dd>

Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpDelete*. Il rettangolo specifica la parte di ogni fotogramma da eliminare. Quando si usa questo flag, il frame viene mantenuto nell'area di lavoro e l'area specificata dal rettangolo diventa nera. Se il flag viene omesso, MCI \_ Delete viene impostato sull'intero frame e il frame viene rimosso dall'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>\_ \_ flusso audio di eliminazione DGV \_ MCI \_
</dt> <dd>

Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpDelete*. Se si usa questo flag e si vuole anche eliminare il video, è necessario usare anche il \_ \_ flag DGV Delete \_ video \_ Stream. Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono eliminati.

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_ \_ \_ flusso video DGV Delete \_ MCI
</dt> <dd>

Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpDelete*. Se si utilizza questo flag e si desidera eliminare anche l'audio, è necessario utilizzare anche il \_ \_ flag del \_ flusso audio DGV Delete MCI \_ . Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono eliminati.

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpDelete*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpDelete*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpDelete* punta a una [**struttura \_ DGV \_ Delete \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .

I flag seguenti si applicano al tipo di dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpDelete*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del [ \_ set di MCI](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpDelete*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .

</dd> </dl>

Per i dispositivi Waveform-Audio, il parametro *lpDelete* punta a una struttura [**\_ \_ \_ parametri Wave Delete MCI**](mci-wave-delete-parms.md) .

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

 

