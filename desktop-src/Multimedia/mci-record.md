---
title: MCI_RECORD comando (Mmsystem.h)
description: Il comando MCI RECORD avvia la registrazione dalla posizione corrente o da una \_ posizione specificata a un'altra posizione specificata.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD comando Windows Multimedia
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
ms.openlocfilehash: 327b9ed9b138b581bec17d8bfcfe19ae67bb07d59be2781af54e22a85e2133c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803452"
---
# <a name="mci_record-command"></a>Comando MCI \_ RECORD

Il [**comando MCI \_ RECORD**](mci-record-parms.md) avvia la registrazione dalla posizione corrente o da una posizione specificata a un'altra posizione specificata. I dispositivi vcr e waveform-audio riconoscono questo comando. Anche se anche i dispositivi video digitali e i sequencer MIDI riconoscono questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Puntatore a [**una struttura MCI \_ RECORD \_ PARMS.**](mci-record-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando è supportato dai dispositivi che restituiscono **TRUE** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il flag MCI \_ GETDEVCAPS \_ CAN \_ RECORD. Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ RECORD:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Una posizione iniziale è inclusa nel **membro dwFrom** della struttura identificata da *lpRecord*. Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Se l'opzione MCI \_ FROM non è specificata, la posizione iniziale viene impostata per impostazione predefinita sulla posizione corrente.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>INSERIMENTO RECORD MCI \_ \_
</dt> <dd>

Le informazioni appena registrate devono essere inserite o incollate nei dati esistenti. Alcuni dispositivi potrebbero non supportare questa funzionalità. Se supportato, questa è l'impostazione predefinita.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>SOVRASCRITTURA RECORD MCI \_ \_
</dt> <dd>

I dati devono sovrascrivere i dati esistenti. L'oggetto MCIWAVE. Il dispositivo DRV restituisce MCIERR \_ UNSUPPORTED \_ FUNCTION in risposta a questo flag.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Una posizione finale è inclusa nel **membro dwTo** della struttura identificata da *lpRecord*. Le unità assegnate ai valori di posizione vengono specificate con il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Se l'opzione MCI TO non è specificata, il percorso finale viene \_ utilizzato per impostazione predefinita alla fine del contenuto.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>FLUSSO AUDIO DI \_ REGISTRAZIONE MCI DGV \_ \_ \_
</dt> <dd>

Un numero di flusso audio è incluso nel **membro dwAudioStream** della struttura identificata da *lpRecord*. Se si omette questo flag, i dati audio vengono registrati nel primo flusso fisico.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>BLOCCO RECORD \_ MCI DGV \_ \_
</dt> <dd>

Quando la registrazione si arresta, lo schermo contenerà l'ultima immagine e non riprenderà a visualizzare il video fino a quando non viene eseguito un comando [MCI \_ MONITOR.](mci-monitor.md)

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>FLUSSO VIDEO DI \_ REGISTRAZIONE MCI DGV \_ \_ \_
</dt> <dd>

Un numero di flusso video è incluso nel **membro dwVideoStream** della struttura identificata da *lpRecord*. Se si omette questo flag, i dati video vengono registrati nel primo flusso fisico.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Un rettangolo viene specificato nel **membro rc** della struttura identificata da *lpRecord*. Il rettangolo specifica l'area dell'input esterno usato come origine per i pixel compressi e salvati. Il valore predefinito di questo rettangolo è il rettangolo specificato (o predefinito) dal flag MCI \_ DGV \_ PUT VIDEO per il comando \_ [MCI \_ PUT.](mci-put.md) Quando è impostato in modo diverso rispetto al rettangolo video, ciò che viene visualizzato non è ciò che viene registrato

</dd> </dl>

Per i dispositivi video digitali, *lpRecord* punta a una [**struttura MCI \_ DGV \_ RECORD \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>RECORD DEL VCR MCI \_ \_ \_ IN
</dt> <dd>

Il **membro dwAt** della struttura identificata da *lpRecord* contiene un'ora in cui inizia l'intero comando o se il dispositivo viene cued, quando il dispositivo raggiunge la posizione da specificata dal comando cue.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>INIZIALIZZAZIONE \_ DEL RECORD DEL \_ VCR MCI \_
</dt> <dd>

Cercare il dispositivo all'inizio del supporto, iniziare a registrare video e audio vuoti e registrare il codice temporale, se possibile.

</dd> </dl>

Per i dispositivi VCR, *lpRecord* punta a [**una struttura MCI \_ VCR RECORD \_ \_ PARMS.**](mci-vcr-record-parms.md)

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

 

