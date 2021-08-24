---
title: MCI_DELETE comando (Mmsystem.h)
description: Il comando MCI \_ DELETE rimuove i dati dal file. I dispositivi audio e video digitale e waveform riconoscono questo comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE comando Windows Multimedia
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
ms.openlocfilehash: ada80894f9260d0c37323d645694e10b0bcef92e52ebd670764bb9a0c436f837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784581"
---
# <a name="mci_delete-command"></a>Comando MCI \_ DELETE

Il comando MCI \_ DELETE rimuove i dati dal file. I dispositivi audio e video digitale e waveform riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi video digitali, MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Puntatore a una [**struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag seguenti si applicano al **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ DELETE \_ AT
</dt> <dd>

Un rettangolo è incluso nel **membro rc** della struttura identificata da *lpDelete.* Il rettangolo specifica la parte di ogni frame da eliminare. Quando si usa questo flag, il frame viene mantenuto nell'area di lavoro e l'area specificata dal rettangolo diventa nera. Se il flag viene omesso, MCI DELETE viene impostato sull'intero frame e \_ il frame viene rimosso dall'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ DELETE \_ AUDIO \_ STREAM
</dt> <dd>

Un numero di flusso audio è incluso nel **membro dwAudioStream** della struttura identificata *da lpDelete.* Se si usa questo flag e si vuole eliminare anche il video, è necessario usare anche il flag MCI \_ DGV \_ DELETE \_ VIDEO \_ STREAM. Se non viene specificato alcun flag, i dati di tutti i flussi audio e video vengono eliminati.

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ DELETE \_ VIDEO \_ STREAM
</dt> <dd>

Un numero di flusso video è incluso nel **membro dwVideoStream** della struttura identificata *da lpDelete.* Se si usa questo flag e si vuole eliminare anche l'audio, è necessario usare anche il flag MCI \_ DGV \_ DELETE \_ AUDIO \_ STREAM. Se non viene specificato alcun flag, i dati di tutti i flussi audio e video vengono eliminati.

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Una posizione iniziale è inclusa nel **membro dwFrom** della struttura identificata da *lpDelete.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Una posizione finale è inclusa nel **membro dwTo** della struttura identificata da *lpDelete.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT di \_ \_ MCI \_ SET.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpDelete* punta a una [**struttura MCI \_ DGV \_ DELETE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)

I flag seguenti si applicano al **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Una posizione iniziale è inclusa nel **membro dwFrom** della struttura identificata da *lpDelete.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT di \_ \_ [MCI \_ SET](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Una posizione finale è inclusa nel **membro dwTo** della struttura identificata da *lpDelete.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT di \_ \_ MCI \_ SET.

</dd> </dl>

Per i dispositivi audio waveform, il *parametro lpDelete* punta a una [**struttura MCI WAVE DELETE \_ \_ \_ PARMS.**](mci-wave-delete-parms.md)

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

 

