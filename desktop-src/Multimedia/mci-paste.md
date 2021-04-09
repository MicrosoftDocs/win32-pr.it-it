---
title: Comando MCI_PASTE (mmsystem. h)
description: Il \_ comando MCI paste Incolla i dati dagli Appunti in un file. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Comando MCI_PASTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739826"
---
# <a name="mci_paste-command"></a>\_Comando di Incolla MCI

Il \_ comando MCI paste Incolla i dati dagli Appunti in un file. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_Incolla DGV \_ MCI \_ in
</dt> <dd>

Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpPaste*. I primi due valori del rettangolo specificano il punto all'interno del frame in cui inserire le informazioni degli Appunti. Se l'altezza e la larghezza del rettangolo sono diversi da zero, il contenuto degli Appunti viene ridimensionato a tali dimensioni quando vengono incollate nel frame. Se il flag viene omesso, \_ l'impostazione predefinita di MCI paste viene impostata sull'intero rettangolo del frame.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>\_ \_ \_ flusso audio incolla DGV \_ MCI
</dt> <dd>

Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpPaste*. Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel flusso designato. Se negli Appunti è presente più di un flusso audio, il flusso indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare il video, è necessario usare anche il \_ \_ flag di flusso del video DGV paste MCI \_ \_ . Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video. Ogni flusso incollato mantiene il numero di flusso originale.

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_inserimento di DGV per MCI \_ \_
</dt> <dd>

I dati degli Appunti devono essere inseriti nell'area di lavoro esistente in corrispondenza della posizione specificata dall'oggetto MCI \_ da contrassegnare. Tutti i dati esistenti dopo il punto di inserimento vengono spostati nell'area di lavoro per creare spazio. Questo è il valore predefinito.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>\_sovrascrittura \_ Incolla DGV MCI \_
</dt> <dd>

I dati degli Appunti devono sostituire i dati già presenti nell'area di lavoro. I dati dell'area di lavoro sostituiti seguono il punto di inserimento.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_ \_ \_ flusso video incolla DGV \_ MCI
</dt> <dd>

Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpPaste*. Se negli Appunti è presente un solo flusso video, i dati video vengono incollati nel flusso designato. Se negli Appunti è presente più di un flusso video, il flusso indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare l'audio, è necessario usare anche il \_ \_ flag di \_ flusso audio DGV incolla MCI \_ . Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video. Ogni flusso incollato mantiene il numero di flusso originale.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Un valore di posizione è incluso nel membro **dwTo** della struttura identificata da *lpPaste*. Il valore position specifica la posizione in cui iniziare a incollare i dati nell'area di lavoro. Se questo flag viene omesso, per impostazione predefinita la posizione corrisponde alla posizione corrente.

</dd> </dl>

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

 

