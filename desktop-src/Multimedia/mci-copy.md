---
title: MCI_COPY comando (Mmsystem.h)
description: Il comando MCI \_ COPY copia i dati negli Appunti. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039291"
---
# <a name="mci_copy-command"></a>Comando MCI \_ COPY

Il comando MCI \_ COPY copia i dati negli Appunti. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Puntatore a [**una struttura MCI \_ DGV \_ COPY \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV \_ COPY \_ AT
</dt> <dd>

Un rettangolo è incluso nel **membro rc** della struttura identificata da *lpCopy.* Il rettangolo specifica la parte di ogni frame da copiare. Se il flag viene omesso, MCI \_ COPY copia l'intero frame.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ COPY \_ AUDIO \_ STREAM
</dt> <dd>

Un numero di flusso audio è incluso nel **membro dwAudioStream** della struttura identificata da *lpCopy.* Se si usa questo flag e si vuole anche copiare video, è necessario usare anche il flag MCI \_ DGV \_ COPY \_ VIDEO \_ STREAM. Se non viene specificato alcun flag, vengono copiati i dati di tutti i flussi audio e video.

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ COPY \_ VIDEO \_ STREAM
</dt> <dd>

Un numero di flusso video è incluso nel **membro dwVideoStream** della struttura identificata da *lpCopy.* Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il flag MCI \_ DGV \_ COPY \_ AUDIO \_ STREAM. Se non viene specificato alcun flag, vengono copiati i dati di tutti i flussi audio e video.

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Una posizione iniziale è inclusa nel **membro dwFrom** della struttura identificata da *lpCopy.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Un percorso finale è incluso nel **membro dwTo** della struttura identificata da *lpCopy.* Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT del comando \_ \_ MCI \_ SET.

</dd> </dl>

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

 

