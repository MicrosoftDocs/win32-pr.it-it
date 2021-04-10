---
title: Comando MCI_CUT (mmsystem. h)
description: Il \_ comando MCI Cut rimuove i dati dal file e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Comando MCI_CUT Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964530"
---
# <a name="mci_cut-command"></a>\_Comando taglia MCI

Il \_ comando MCI Cut rimuove i dati dal file e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri DGV Cut di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV \_ di MCI Cut \_
</dt> <dd>

Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpCut*. Il rettangolo specifica la parte di ogni fotogramma da tagliare. Se il flag viene omesso, \_ il taglio MCI taglia l'intero frame.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_ \_ \_ flusso audio taglia DGV \_ MCI
</dt> <dd>

Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpCut*. Se si usa questo flag e si vuole anche tagliare il video, è necessario usare anche il \_ flag di flusso del video di MCI DGV \_ Cut \_ \_ . Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono tagliati.

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ \_ flusso video DGV di MCI Cut \_
</dt> <dd>

Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpCut*. Se si usa questo flag e si vuole anche tagliare audio, è necessario usare anche il \_ flag del \_ flusso audio DGV Cut MCI \_ \_ . Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono tagliati.

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpCut*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpCut*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .

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

 

