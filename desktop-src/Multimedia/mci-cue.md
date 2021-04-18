---
title: Comando MCI_CUE (mmsystem. h)
description: Il \_ comando MCI Cue viene segnalato da un dispositivo in modo che la riproduzione o la registrazione inizi con un ritardo minimo. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Comando MCI_CUE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302029"
---
# <a name="mci_cue-command"></a>\_Comando MCI cue

Il \_ comando MCI Cue viene segnalato da un dispositivo in modo che la riproduzione o la registrazione inizi con un ritardo minimo. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_ \_ input cue DGV \_ MCI
</dt> <dd>

Un'istanza di video digitale dovrebbe prepararsi per la registrazione. Se l'applicazione non dispone di spazio su disco riservato, il dispositivo riserva lo spazio su disco usando i parametri predefiniti. L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'input esterno. Questo flag non ha alcun effetto sulla selezione dell'origine della presentazione.

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>\_DGV \_ cue \_ noshow MCI
</dt> <dd>

Un'istanza di video digitale dovrebbe prepararsi a riprodurre il frame specificato con il comando senza visualizzarlo. Quando questo flag viene specificato, la visualizzazione continua a mostrare l'immagine nel buffer del frame anche se il frame corrispondente non è la posizione corrente. Se, ad esempio, il buffer del frame contiene l'immagine del frame 7, il dispositivo continua a visualizzare il frame 7 quando questo flag viene usato per posizionare il dispositivo in un'altra posizione. Un comando cue successivo senza questo flag e senza il \_ flag MCI to Visualizza il frame corrente.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>\_output del \_ cue \_ DGV MCI
</dt> <dd>

Un'istanza di video digitale dovrebbe prepararsi per la riproduzione. Se l'area di lavoro è sospesa, non viene eseguito alcun posizionamento. Se l'area di lavoro viene arrestata, la posizione potrebbe cambiare in un'immagine del fotogramma chiave precedente. L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'area di lavoro.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione dell'area di lavoro è inclusa nel membro **dwTo** della struttura identificata da *lpCue*. Le unità assegnate ai valori di posizione vengono specificate usando il \_ \_ \_ flag di formato dell'ora del set di MCI del comando [ \_ set di MCI](mci-set.md) . Questa operazione equivale alla ricerca di una posizione, ad eccezione del fatto che il dispositivo viene sospeso dopo il comando.

</dd> </dl>

Per i dispositivi **digitalvideo** , il parametro *lpCue* punta a una struttura [**\_ DGV \_ cue \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Il membro **dwFrom** della struttura a cui punta *lpCue* contiene la posizione iniziale specificata nel formato dell'ora corrente.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Il membro **dwTo** della struttura a cui punta *lpCue* contiene la posizione finale (sospensione) specificata nel formato dell'ora corrente.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_input di \_ cue \_ VCR MCI
</dt> <dd>

Prepararsi per la registrazione.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_output di \_ cue \_ VCR per MCI
</dt> <dd>

Prepararsi per la riproduzione. Se non è stato specificato né l'output della cue VCR MCI \_ \_ né l' \_ \_ \_ \_ output di cue VCR, \_ \_ viene utilizzato l'output di cue VCR \_ per MCI.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>preroll di \_ cue VCR di MCI \_ \_
</dt> <dd>

Cue il dispositivo alla posizione corrente o alla posizione **dwFrom** , meno la durata della preregistrazione. Questo consentirà al dispositivo di prepararsi prima di entrare in modalità registrazione o riproduzione.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>\_ \_ segnale \_ inverso del VCR MCI
</dt> <dd>

La direzione del comando Play o record successivo è inversa.

</dd> </dl>

Quando si esegue il ripasso per la riproduzione usando il \_ comando MCI cue con il \_ contrassegno MCI VCR \_ cue \_ output, è possibile annullare \_ la cue MCI eseguendo il comando [MCI \_ Play](mci-play.md) con MCI \_ from, MCI \_ to o MCI \_ VCR \_ Play \_ Reverse.

Quando si esegue il ripasso per la registrazione tramite MCI \_ cue con il \_ contrassegno MCI VCR \_ cue \_ input flag, è possibile annullare \_ la cue MCI inviando il comando [MCI \_ record](mci-record.md) con MCI \_ from, MCI \_ to o MCI \_ VCR \_ record \_ Initialize.

Per i dispositivi **VCR** , il parametro *lpCue* punta a una struttura [**\_ \_ \_ parametri cue VCR di MCI**](mci-vcr-cue-parms.md) .

Con il tipo di dispositivo **WaveAudio** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI
</dt> <dd>

Un dispositivo di input della forma d'onda-audio deve essere sottomesso A cue.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI
</dt> <dd>

Un dispositivo di output della forma d'onda-audio deve essere riprodotto. Si tratta del flag predefinito se non è specificato alcun flag.

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

 

