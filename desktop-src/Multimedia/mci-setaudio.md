---
title: MCI_SETAUDIO comando (Mmsystem.h)
description: Il comando MCI \_ SETAUDIO imposta i valori associati alla riproduzione e all'acquisizione audio. I dispositivi video e videoregistratori digitali riconoscono questo comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882209b8a9debc2c01e4f5c6f852d418c1a5cd321a764af022d19c58fe32a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803398"
---
# <a name="mci_setaudio-command"></a>Comando MCI \_ SETAUDIO

Il comando MCI \_ SETAUDIO imposta i valori associati alla riproduzione e all'acquisizione audio. I dispositivi video e videoregistratori digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag seguenti si applicano al **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG
</dt> <dd>

Il **membro lpstrAlgorithm** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione audio. L'algoritmo di compressione viene usato dai comandi [MCI \_ RESERVE](mci-reserve.md) o [MCI \_ RECORD successivi.](mci-record.md) Gli algoritmi disponibili dipendono dal dispositivo. Se l'algoritmo non è compatibile con il formato di file corrente, il formato di file viene modificato nel formato predefinito per l'algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

Il tempo specificato è espresso in millisecondi ed è il tempo assoluto se usato con MCI \_ DGV \_ SETAUDIO \_ OVER. Questa volta non è in esecuzione la riproduzione dell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI \_ DGV \_ SETAUDIO \_ INPUT
</dt> <dd>

Modifica il flag bass, acuto o volume in modo che influisca sul segnale di input e modifichi ciò che viene registrato. Se possibile, si tratta dell'impostazione predefinita quando si monitora l'input.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>ELEMENTO MCI \_ DGV \_ SETAUDIO \_
</dt> <dd>

Una costante audio viene specificata nel **membro dwItem** della struttura identificata da *lpSetAudio*. La costante identifica il valore impostato. Sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

Il numero medio di byte viene specificato nel **membro dwValue** della struttura identificata da *lpSetAudio*. Questo valore imposta il numero medio di byte al secondo per la riproduzione o la registrazione nei formati PCM (Pulse Code Modulation) e ADPCM (Adaptive Differential Pulse Code Modulation). Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ BASS
</dt> <dd>

Il livello di bassa frequenza audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BITSPERSAMPLE
</dt> <dd>

Il numero di bit per campione è specificato nel **membro dwValue** della struttura identificata da *lpSetAudio*. Questo valore imposta il numero di bit per campione riprodotto o registrato nel formato PCM. Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

L'allineamento del blocco di dati è specificato nel **membro dwValue** della struttura identificata da *lpSetAudio*. Questo valore imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati della forma d'onda di input.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>ESEMPI DI \_ MCI DGV \_ SETAUDIOPERSEC \_
</dt> <dd>

La frequenza di campionamento è specificata nel **membro dwValue** della struttura identificata da *lpSetAudio*. Questo valore imposta la frequenza di campionamento per la riproduzione e la registrazione con gli algoritmi PCM e ADPCM. Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>ORIGINE MCI \_ DGV \_ SETAUDIO \_
</dt> <dd>

Una costante che specifica l'origine dell'input audio è inclusa nel **membro dwValue** della struttura identificata da *lpSetAudio*. Per le origini di input audio sono definite le costanti seguenti:

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ AVERAGE

Media dei canali audio sinistro e destro.

ORIGINE MCI \_ DGV \_ SETAUDIO \_ \_ SINISTRA

Canale audio sinistro.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ RIGHT

Canale audio destro.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ STEREO

Stereo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>FLUSSO \_ \_ SETAUDIO MCI \_ DGV
</dt> <dd>

Un flusso audio viene specificato nel **membro dwValue** della struttura identificata da *lpSetAudio*. Il valore intero specifica il flusso audio riprodotto dall'area di lavoro. Se il flusso non viene specificato, viene riprodotto il primo flusso audio interleaved fisicamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ TREBLE
</dt> <dd>

Il livello di frequenza elevata audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI \_ DGV \_ SETAUDIO \_ VOLUME
</dt> <dd>

Il livello audio per uno o entrambi i canali audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*. Se i volumi sinistro e destro sono stati impostati su valori diversi, il rapporto tra volume da sinistra a destra rimane approssimativamente invariato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ A SINISTRA
</dt> <dd>

Abilita il canale audio sinistro se usato con MCI \_ SET \_ ON. Disabilita il canale audio sinistro quando viene usato con MCI \_ SET \_ OFF. Quando questo flag viene usato con la combinazione di \_ MCI DGV \_ SETAUDIO VALUE e \_ MCI \_ DGV \_ SETAUDIO VOLUME, imposta il volume del \_ canale audio sinistro. Quando questo flag viene usato con MCI \_ DGV SETAUDIO SOURCE, specifica il canale audio sinistro come origine per il \_ digitalizzatore di input \_ audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_ OVER
</dt> <dd>

Un parametro di lunghezza della transizione è incluso nel **membro dwOver** della struttura identificata da *lpSetAudio*. Il valore length specifica per quanto tempo (in unità del formato ora corrente) deve essere necessario apportare una modifica che usa un fattore. Se questo flag non viene usato, le modifiche vengono apportate immediatamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ SETAUDIO \_ QUALITY
</dt> <dd>

Il **membro lpstrQuality** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer che definisce la qualità audio. Una stringa di testo all'interno del buffer specifica le caratteristiche dell'algoritmo di compressione audio.

Il flag MCI DGV SETAUDIO ALG può essere usato per selezionare un descrittore di qualità \_ \_ per \_ l'algoritmo specificato. Se questo flag viene omesso, viene usato l'algoritmo corrente.

Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo. Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi dei descrittori applicabili. Il [comando MCI \_ QUALITY](mci-quality.md) può definire nomi di descrittori aggiuntivi.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI \_ DGV \_ SETAUDIO \_ RECORD
</dt> <dd>

Specifica se la registrazione include o esclude i dati audio. In combinazione con MCI \_ SET \_ ON, vengono registrati i dati audio. In combinazione con MCI \_ SET \_ OFF, i dati audio vengono esclusi. L'impostazione predefinita include i dati audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Abilita il canale audio giusto se usato con MCI \_ SET \_ ON. Disabilita il canale audio giusto se usato con MCI \_ SET \_ OFF. Quando questo flag viene usato con la combinazione di \_ MCI DGV \_ SETAUDIO VALUE e \_ MCI \_ DGV \_ SETAUDIO VOLUME, imposta il volume del \_ canale audio giusto.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>VALORE DI \_ MCI DGV \_ SETAUDIO \_
</dt> <dd>

Un valore viene specificato nel **membro dwValue** della struttura identificata da *lpSetAudio.* Il significato del valore viene specificato dalla costante definita per il \_ flag MCI DGV \_ SETAUDIO \_ ITEM.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Disabilita il canale audio specificato.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Abilita il canale audio specificato.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>OUTPUT \_ DI MCI SETAUDIO \_
</dt> <dd>

Modifica il flag di volume, acuto o acuto in modo che modifichi solo il segnale riprodotto e non ciò che viene registrato. Se possibile, questa è l'impostazione predefinita quando si monitora l'input.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpSetAudio* punta a una [**struttura \_ MCI DGV \_ SETAUDIO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>RECORD \_ \_ SETAUDIO DEL VCR MCI \_
</dt> <dd>

Imposta la registrazione audio su on o off, che viene usata in combinazione con uno dei flag seguenti:

MCI \_ SET \_ ON

Registrazione audio.

MCI \_ SET \_ OFF

Registrazione audio disattivata. Potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ SET](mci-set.md) con il flag MCI VCR SET ASSEMBLE RECORD impostato su off) prima che la registrazione audio possa \_ essere \_ \_ \_ disattivata.

MCI \_ TRACK

Il **membro dwTrack** della struttura identificata da *lpSetAudio* specifica quale traccia è interessata dal comando.

MCI \_ VCR \_ SETAUDIO \_ SOURCE

Imposta l'origine audio. Questo flag deve essere usato con il \_ flag MCI VCR \_ SETAUDIO \_ TO.

MCI \_ VCR \_ SETAUDIO \_ MONITOR

Imposta il monitor di origine audio. Questo flag deve essere usato con il \_ flag MCI VCR \_ SETAUDIO \_ TO.

MCI \_ VCR \_ SETAUDIO \_ TO

Il **membro dwTo** della struttura identificata da *lpSetAudio* contiene una costante che descrive il tipo di input o l'input monitorato. Deve essere uno dei seguenti:

<dl> <dd>

SINER \_ DI TIPO MCI VCR \_ \_ \_ SRC

Il tipo è tuner.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ LINE

Il tipo è line.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ AUX

Il tipo è ausiliario.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC

Il tipo è generico.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ MUTE

Il tipo è mute. Può essere usato solo con il \_ flag MCI VCR \_ SETAUDIO \_ SOURCE.

</dd> <dd>

OUTPUT DEL TIPO \_ SRC DEL VCR MCI \_ \_ \_

Il tipo viene restituito.

</dd> <dd>

MCI \_ VCR \_ SETAUDIO \_ NUMBER

Il membro dwNumber della struttura identificata da lpSetAudio contiene l'input audio (del tipo specificato nel membro dwTo) da usare.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Per i dispositivi VCR, il *parametro lpSetAudio* punta a una [**struttura \_ MCI VCR \_ SETAUDIO \_ PARMS.**](mci-vcr-setaudio-parms.md)

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

 

