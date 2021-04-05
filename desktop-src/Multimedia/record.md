---
title: comando record
description: Il comando record avvia la registrazione dei dati. VCR e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- registrare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873349"
---
# <a name="record-command"></a>comando record

Il comando record avvia la registrazione dei dati. VCR e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Flag per la registrazione dei dati. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **registra** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                | Significato                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | al *flusso* del flusso audio *rettangolare* dalla *posizione* in attesa | Inserisci Sovrascrivi per *posizionare* il *flusso* del flusso video |
| sequencer    | da *position* Insert                                  | Sovrascrivi in *posizione*                             |
| VCR          | al *momento* dall'inizializzazione della *posizione*                     | Inserisci sovrascrittura nella *posizione*                      |
| WaveAudio    | da *position* Insert                                  | Sovrascrivi in *posizione*                             |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRecordFlags** e i relativi significati.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo*        | Specifica un'area rettangolare dell'input esterno usato come origine per i pixel compressi e salvati. Se non specificato, per impostazione predefinita il rettangolo è il rettangolo specificato per [put](put.md) "video". Quando viene impostato in modo diverso rispetto al rettangolo "video", l'immagine visualizzata non è quella registrata. |
| al *momento*             | Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando. Per ulteriori informazioni, vedere il comando [cue](cue.md) .                                                                                                                             |
| *flusso* del flusso audio | Specifica il flusso audio usato per la registrazione. Se questo flag non è specificato e il formato di file non definisce un valore predefinito, viene registrato nel flusso fisicamente per primo.                                                                                                                             |
| dalla *posizione*       | Specifica una posizione iniziale per la registrazione. Se il flag "from" non è specificato, il dispositivo avvia la registrazione nella posizione corrente.                                                                                                                                                                       |
| contenere                  | Blocca l'immagine al termine della registrazione anziché visualizzare il video in tempo reale. Quando la registrazione viene arrestata, viene eseguito un comando di [monitoraggio](monitor.md) automatico "file". Per tornare al video live, eseguire il comando **Monitor** "input".                                                                              |
| inizializzazione            | Inizializzare il nastro (supporto), che prevede la registrazione del codice temporale (se possibile) per video e audio vuoti. Questo comando può richiedere diverse ore se è necessario inizializzare l'intero nastro.                                                                                                                            |
| insert                | Specifica che i nuovi dati vengono aggiunti al file nella posizione corrente.                                                                                                                                                                                                                                            |
| overwrite             | Consente di specificare che i nuovi dati sostituiranno i dati nel file.                                                                                                                                                                                                                                                           |
| *posizione*         | Specifica una posizione finale per la registrazione. Se il flag "to" non è specificato, il dispositivo viene registrato fino a quando non viene ricevuto un comando [Stop](stop.md) o [pause](pause.md) .                                                                                                                                        |
| *flusso* del flusso video | Specifica il flusso video usato per la registrazione. Se questo parametro non viene specificato e il formato del file non definisce un valore predefinito, viene registrato nel flusso fisicamente per primo.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La registrazione si interrompe quando viene eseguito un comando di [arresto](stop.md) o [sospensione](pause.md) . Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.

Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) . Le tracce da registrare sono specificate dal [setimecode](settimecode.md) "record", impostare i comandi "assembla record", [sevideo](setvideo.md) "record [" e "record".](setaudio.md)

## <a name="examples"></a>Esempio

Il comando seguente avvia la registrazione nella posizione corrente.

``` syntax
record mysound
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[segnale](cue.md)
</dt> <dt>

[monitoraggio](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[mettere](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[codice temporale](settimecode.md)
</dt> <dt>

[video](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

