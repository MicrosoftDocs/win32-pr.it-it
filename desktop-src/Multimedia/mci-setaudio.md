---
title: Comando MCI_SETAUDIO (mmsystem. h)
description: Il \_ comando MCI seaudio imposta i valori associati alla riproduzione audio e all'acquisizione. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Comando MCI_SETAUDIO Windows Multimedia
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
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225230"
---
# <a name="mci_setaudio-command"></a>\_Comando MCI SEfonica

Il \_ comando MCI seaudio imposta i valori associati alla riproduzione audio e all'acquisizione. I dispositivi Digital-video e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag seguenti si applicano al tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ sefonica \_ ALG
</dt> <dd>

Il membro **lpstrAlgorithm** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione audio. L'algoritmo di compressione viene usato dai comandi di [ \_ riserva MCI](mci-reserve.md) o del [ \_ record MCI](mci-record.md) successivi. Gli algoritmi disponibili sono dipendenti dal dispositivo. Se l'algoritmo non è compatibile con il formato di file corrente, il formato del file viene modificato nel formato predefinito per l'algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>\_CLOCKTIME DGV \_ di MCI \_
</dt> <dd>

Il tempo specificato è in millisecondi ed è il tempo assoluto se usato con \_ DGV di MCI \_ \_ . Questa volta non è al passo con la riproduzione dell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_input di DGV MCI \_ \_
</dt> <dd>

Modifica il flag Bass, Treble o volume in modo che influisca sul segnale di input e modifichi gli elementi registrati. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_elemento DGV \_ di MCI \_
</dt> <dd>

Una costante audio è specificata nel membro **dwItem** della struttura identificata da *lpSetAudio*. La costante identifica il valore che viene impostato. Sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>\_AVGBYTESPERSEC DGV \_ di MCI \_
</dt> <dd>

Il numero medio di byte viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*. Questo valore consente di impostare il numero medio di byte al secondo per la riproduzione o la registrazione nei formati PCM (Pulse Code Modulation) e ADPCM (Adaptive differenziale Code Modulation). Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>\_Bass DGV \_ MCI \_
</dt> <dd>

Il livello di frequenza bassa audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>\_BitsPerSample DGV \_ di MCI \_
</dt> <dd>

Il numero di bit per campione viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*. Questo valore consente di impostare il numero di bit per campione riprodotto o registrato nel formato PCM. Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>\_BLOCKALIGN DGV \_ di MCI \_
</dt> <dd>

L'allineamento dei blocchi di dati viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*. Questo valore imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati della forma d'onda di input.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>\_SAMPLESPERSEC DGV \_ di MCI \_
</dt> <dd>

La frequenza di campionamento è specificata nel membro **dwValue** della struttura identificata da *lpSetAudio*. Questo valore consente di impostare la frequenza di campionamento per la riproduzione e la registrazione con gli algoritmi PCM e ADPCM. Il file viene salvato in questo formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_origine DGV \_ MCI \_
</dt> <dd>

Una costante che specifica l'origine dell'input audio è inclusa nel membro **dwValue** della struttura identificata da *lpSetAudio*. Per le origini di input audio sono definite le costanti seguenti:

\_ \_ \_ media origine DGV MCI \_

Media dei canali audio sinistro e destro.

\_origine DGV \_ \_ di MCI \_

Canale audio sinistro.

DGV di origine del file MCI- \_ \_ \_ \_ right

Canale audio corretto.

\_stereo di \_ origine DGV \_ MCI \_

Stereo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flusso DGV \_ MCI \_
</dt> <dd>

Un flusso audio viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*. Il valore integer specifica il flusso audio riprodotto dall'area di lavoro. Se il flusso non è specificato, viene riprodotto il primo flusso audio con interfoliazione fisico.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>gli \_ \_ acuti DGV di MCI \_
</dt> <dd>

Il livello di frequenza elevata audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volume DGV \_ MCI \_
</dt> <dd>

Il livello audio per uno o entrambi i canali audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*. Se i volumi sinistro e destro sono stati impostati su valori diversi, il rapporto tra il volume da sinistra a destra è approssimativamente invariato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ \_ Left
</dt> <dd>

Abilita il canale audio sinistro se usato con MCI \_ impostato \_ su. Disabilita il canale audio sinistro se usato con MCI \_ impostato su \_ off. Quando questo flag viene usato con la combinazione di \_ DGV \_ \_ e MCI DGV del volume MCI \_ \_ \_ , imposta il volume del canale audio sinistro. Quando questo flag viene usato con l' \_ \_ \_ origine DGV di MCI, specifica il canale audio sinistro come origine per il digitalizzatore di input audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>\_DGV MCI \_ \_
</dt> <dd>

Un parametro della lunghezza della transizione è incluso nel membro **dwOver** della struttura identificata da *lpSetAudio*. Il valore length specifica la durata (in unità del formato dell'ora corrente) da eseguire per apportare una modifica che utilizza un fattore. Se questo flag non viene utilizzato, le modifiche vengono eseguite immediatamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_qualità dell' \_ audio DGV \_ MCI
</dt> <dd>

Il membro **lpstrQuality** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer che definisce la qualità audio. Una stringa di testo all'interno del buffer specifica le caratteristiche dell'algoritmo di compressione audio.

Per \_ \_ \_ selezionare un descrittore di qualità per l'algoritmo specificato, è possibile usare il flag DGV di MCI. Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.

Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo. Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi di descrittori applicabili. Il comando [MCI \_ Quality](mci-quality.md) può definire nomi di descrittori aggiuntivi.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_record DGV \_ MCI \_
</dt> <dd>

Specifica se la registrazione include o esclude i dati audio. In combinazione con MCI \_ impostato \_ su, vengono registrati i dati audio. In combinazione con MCI \_ impostato su \_ disattivato, i dati audio vengono esclusi. Il valore predefinito include i dati audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>DGV MCI a \_ \_ \_ destra
</dt> <dd>

Abilita il canale audio corretto se usato con MCI \_ impostato \_ su. Disattiva il canale audio corretto se usato con MCI \_ impostato su \_ off. Quando questo flag viene usato con la combinazione di \_ DGV \_ \_ e MCI DGV del volume MCI \_ \_ \_ , imposta il volume del canale audio corretto.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_valore di DGV MCI \_ \_
</dt> <dd>

Viene specificato un valore nel membro **dwValue** della struttura identificata da *lpSetAudio*. Il significato del valore viene specificato dalla costante definita per il \_ flag di elemento DGV di MCI \_ \_ .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Disabilita il canale audio specificato.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Abilita il canale audio specificato.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>OUTPUT di MCI \_ SEfonica \_
</dt> <dd>

Modifica il flag Bass, Treble o volume in modo che modifichi solo il segnale riprodotto e non quello registrato. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpSetAudio* punta a una struttura [**MCI \_ DGV \_ \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_record di \_ disaudio \_ VCR MCI
</dt> <dd>

Imposta la registrazione audio su on o off, che viene utilizzata insieme a uno dei flag seguenti:

MCI \_ impostato \_ su

Registrazione audio in.

\_set \_ disattivato

Registrazione audio disattivata. Prima di disattivare la registrazione audio, potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ set](mci-set.md) con il \_ flag MCI \_ set \_ assembla \_ record impostato su OFF).

\_traccia MCI

Il membro **dwTrack** della struttura identificata da *lpSetAudio* specifica la traccia interessata dal comando.

\_origine file VCR VCR MCI \_ \_

Imposta l'origine audio. Questo flag deve essere utilizzato con l' \_ \_ \_ opzione per il flag di MCI VCR per il flag.

\_ \_ monitoraggio sefonica VCR \_ MCI

Imposta il monitor di origine audio. Questo flag deve essere utilizzato con l' \_ \_ \_ opzione per il flag di MCI VCR per il flag.

\_VCR VCR MCI \_ \_ per

Il membro **dwTo** della struttura identificata da *lpSetAudio* contiene una costante che descrive il tipo di input o di input monitorato. Deve essere uno dei seguenti:

<dl> <dd>

\_Tuner di \_ \_ tipo src VCR di \_ MCI

Il tipo è Tuner.

</dd> <dd>

\_ \_ \_ riga tipo src VCR \_ MCI

Il tipo è line.

</dd> <dd>

\_ \_ tipo src VCR \_ MCI \_ aux

Il tipo è ausiliario.

</dd> <dd>

\_ \_ tipo src VCR \_ MCI \_ generico

Il tipo è generico.

</dd> <dd>

\_silenziamento del \_ \_ tipo src del VCR \_ MCI

Il tipo è mute. Questa operazione può essere utilizzata solo con il \_ \_ flag di origine sefonica VCR MCI \_ .

</dd> <dd>

\_ \_ \_ output tipo src VCR \_ MCI

Il tipo è output.

</dd> <dd>

\_numero di \_ file VCR \_ VCR MCI

Il membro dwNumber della struttura identificata da lpSetAudio contiene l'input audio (del tipo specificato nel membro dwTo) da usare.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Per i dispositivi VCR, il parametro *lpSetAudio* punta a una struttura [**\_ \_ \_ parametri del videoregistratore MCI**](mci-vcr-setaudio-parms.md) .

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

 

