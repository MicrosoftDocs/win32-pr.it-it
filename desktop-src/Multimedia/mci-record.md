---
title: Comando MCI_RECORD (mmsystem. h)
description: Il \_ comando MCI record avvia la registrazione dalla posizione corrente o da un percorso specificato a un altro percorso specificato.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Comando MCI_RECORD Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119991"
---
# <a name="mci_record-command"></a>\_Comando record MCI

Il comando [**MCI \_ record**](mci-record-parms.md) avvia la registrazione dalla posizione corrente o da un percorso specificato a un altro percorso specificato. VCR e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
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

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri del record MCI**](mci-record-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con MCI \_ GETDEVCAPS \_ can \_ record flag. Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano il \_ record MCI:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpRecord*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) . Se MCI \_ from non è specificato, per impostazione predefinita la posizione iniziale viene impostata sulla posizione corrente.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserimento record \_ MCI
</dt> <dd>

Le informazioni appena registrate devono essere inserite o incollate nei dati esistenti. Alcuni dispositivi potrebbero non supportare questo problema. Se supportato, si tratta dell'impostazione predefinita.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>sovrascrittura del \_ record MCI \_
</dt> <dd>

I dati devono sovrascrivere i dati esistenti. MCIWAVE. Il dispositivo DRV restituisce MCIERR \_ funzione non supportata \_ in risposta a questo flag.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpRecord*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) . Se MCI \_ to non è specificato, il percorso finale viene impostato sul valore predefinito alla fine del contenuto.

</dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_ \_ flusso audio del record DGV \_ MCI \_
</dt> <dd>

Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpRecord*. Se si omette questo flag, i dati audio vengono registrati nel primo flusso fisico.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_ \_ attesa record DGV \_ MCI
</dt> <dd>

Quando la registrazione viene arrestata, la schermata conterrà l'ultima immagine e non riprende a visualizzare il video fino a quando non viene emesso un comando di [ \_ monitoraggio MCI](mci-monitor.md) .

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_ \_ flusso video di record DGV \_ MCI \_
</dt> <dd>

Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpRecord*. Se si omette questo flag, i dati video vengono registrati nel primo flusso fisico.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_
</dt> <dd>

Un rettangolo viene specificato nel membro **RC** della struttura identificata da *lpRecord*. Il rettangolo specifica l'area dell'input esterno usato come origine per i pixel compressi e salvati. Per impostazione predefinita, questo rettangolo è il rettangolo specificato (o predefinito) dal \_ flag DGV \_ put \_ video per il comando [MCI \_ put](mci-put.md) . Quando viene impostato in modo diverso rispetto al rettangolo video, ciò che viene visualizzato non è quello registrato

</dd> </dl>

Per i dispositivi digitali video, *lpRecord* punta a una struttura di [**\_ \_ \_ parametri del record DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_record MCI \_ VCR \_ in
</dt> <dd>

Il membro **dwAt** della struttura identificata da *lpRecord* contiene un'ora di inizio dell'intero comando o se il dispositivo viene riavviato quando il dispositivo raggiunge la posizione dalla posizione specificata dal comando cue.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_ \_ inizializzazione record VCR MCI \_
</dt> <dd>

Cercare il dispositivo all'inizio del supporto, iniziare la registrazione del video e dell'audio vuoti e registrare il timecode, se possibile.

</dd> </dl>

Per i dispositivi VCR, *lpRecord* punta a una struttura [**\_ \_ \_ parametri del record VCR MCI**](mci-vcr-record-parms.md) .

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

 

