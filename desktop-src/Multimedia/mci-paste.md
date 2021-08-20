---
title: MCI_PASTE comando (Mmsystem.h)
description: Il comando MCI \_ PASTE incolla i dati dagli Appunti in un file. I dispositivi video digitali riconoscono questo comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE comando Windows Multimedia
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
ms.openlocfilehash: 3bdc7b27838236b09952a009f1cb8c7d60091afb6634bbd74fad213f013f6e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138232"
---
# <a name="mci_paste-command"></a>Comando MCI \_ PASTE

Il comando MCI \_ PASTE incolla i dati dagli Appunti in un file. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Puntatore a [**una struttura \_ \_ \_ PARMS PASTE MCI DGV.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ PASTE \_ AT
</dt> <dd>

Un rettangolo è incluso nel **membro rc** della struttura identificata da *lpPaste.* I primi due valori del rettangolo specificano il punto all'interno del frame in cui inserire le informazioni degli Appunti. Se l'altezza e la larghezza del rettangolo sono diverse da zero, il contenuto degli Appunti viene ridimensionato in base a tali dimensioni quando vengono incollati nel frame. Se il flag viene omesso, l'opzione MCI \_ PASTE viene impostata per impostazione predefinita sull'intero rettangolo del frame.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ PASTE \_ AUDIO \_ STREAM
</dt> <dd>

Un numero di flusso audio è incluso nel **membro dwAudioStream** della struttura identificata da *lpPaste.* Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel flusso designato. Se negli Appunti sono presenti più flussi audio, il flusso indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare video, è necessario usare anche il flag MCI \_ DGV \_ PASTE \_ VIDEO \_ STREAM. Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video. Ogni flusso incollato mantiene il numero di flusso originale.

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ DGV \_ PASTE \_ INSERT
</dt> <dd>

I dati degli Appunti devono essere inseriti nell'area di lavoro esistente nella posizione specificata dal flag MCI \_ TO. Tutti i dati esistenti dopo il punto di inserimento vengono spostati nell'area di lavoro per fare spazio. Questo è il valore predefinito.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI \_ DGV \_ PASTE \_ OVERWRITE
</dt> <dd>

I dati degli Appunti devono sostituire i dati già presenti nell'area di lavoro. I dati dell'area di lavoro sostituiti seguono il punto di inserimento.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ PASTE \_ VIDEO \_ STREAM
</dt> <dd>

Un numero di flusso video è incluso nel **membro dwVideoStream** della struttura identificata da *lpPaste*. Se negli Appunti è presente un solo flusso video, i dati del video vengono incollati nel flusso designato. Se negli Appunti sono presenti più flussi video, il flusso indica il numero iniziale per le sequenze di flusso. Se si usa questo flag e si vuole anche incollare audio, è necessario usare anche il flag MCI \_ DGV \_ PASTE \_ AUDIO \_ STREAM. Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video. Ogni flusso incollato mantiene il numero di flusso originale.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Un valore di posizione è incluso nel **membro dwTo** della struttura identificata da *lpPaste.* Il valore position specifica la posizione in cui iniziare a incollare i dati nell'area di lavoro. Se questo flag viene omesso, la posizione predefinita è la posizione corrente.

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

 

