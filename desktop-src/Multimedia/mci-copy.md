---
title: Comando MCI_COPY (mmsystem. h)
description: Il \_ comando di copia MCI copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Comando MCI_COPY Windows Multimedia
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
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964280"
---
# <a name="mci_copy-command"></a>\_Comando di copia MCI

Il \_ comando di copia MCI copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Puntatore a una struttura di [**\_ \_ Copia \_ parametri di DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copia di DGV MCI \_ in
</dt> <dd>

Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpCopy*. Il rettangolo specifica la parte di ogni fotogramma da copiare. Se il flag viene omesso, \_ la copia di MCI copia l'intero frame.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_ \_ \_ flusso audio copia DGV \_ MCI
</dt> <dd>

Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpCopy*. Se si usa questo flag e si vuole anche copiare il video, è necessario usare anche il \_ flag di flusso del video DGV della \_ copia MCI \_ \_ . Se non viene specificato alcun flag, vengono copiati i dati provenienti da tutti i flussi audio e video.

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ \_ flusso video copia DGV \_ MCI
</dt> <dd>

Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpCopy*. Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il \_ \_ flag del \_ flusso audio DGV di copia MCI \_ . Se non viene specificato alcun flag, vengono copiati i dati provenienti da tutti i flussi audio e video.

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpCopy*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpCopy*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del \_ comando set di MCI.

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

 

