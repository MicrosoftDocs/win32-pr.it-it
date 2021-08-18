---
title: comando record
description: Il comando di registrazione avvia la registrazione dei dati. I dispositivi videoregistratore e audio waveform riconoscono questo comando. Anche se i dispositivi video digitali e i sequencer MIDI riconoscono anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- Comando record Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f326b13d86f073074ef2c1119d449e297e65e7d3accb22d9858e5c1579493c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037561"
---
# <a name="record-command"></a>comando record

Il comando di registrazione avvia la registrazione dei dati. I dispositivi videoregistratore e audio waveform riconoscono questo comando. Anche se i dispositivi video digitali e i sequencer MIDI riconoscono anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Flag per la registrazione dei dati. La tabella seguente elenca i tipi di dispositivo che **riconoscono** il comando record e i flag usati da ogni tipo.



| Valore        | Significato                                                | Significato                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | flusso *audio del rettangolo* *dalla* *posizione* di attesa | insert overwrite to position video stream stream (Inserisci sovrascrittura *per posizionare* il flusso *video)* |
| sequencer    | from *position* insert                                  | sovrascrivere in *posizione*                             |
| Vcr          | at *time from* *position* initialize                     | insert overwrite to *position*                      |
| Waveaudio    | from *position* insert                                  | sovrascrivere in *posizione*                             |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszRecordFlags** e i relativi significati.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle*        | Specifica un'area rettangolare dell'input esterno usato come origine per i pixel compressi e salvati. Se non specificato, il rettangolo viene utilizzato per impostazione predefinita sul rettangolo specificato per [put](put.md) "video". Quando è impostato in modo diverso dal rettangolo "video", l'immagine visualizzata non è ciò che viene registrato. |
| at *time*             | Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato indicato, quando inizia il comando cued. Per altre informazioni, vedere il [comando cue.](cue.md)                                                                                                                             |
| flusso  audio | Specifica il flusso audio usato per la registrazione. Se questo flag non viene specificato e il formato di file non definisce un valore predefinito, viene registrato nel flusso che viene fisicamente per primo.                                                                                                                             |
| dalla *posizione*       | Specifica una posizione iniziale per la registrazione. Se il flag "from" non è specificato, il dispositivo avvia la registrazione nella posizione corrente.                                                                                                                                                                       |
| Tenere                  | Blocca l'immagine al termine della registrazione anziché visualizzare video live. Quando la registrazione si arresta, viene [eseguito](monitor.md) un comando "file" di monitoraggio automatico. Per tornare al video live, eseguire il **comando** "input" di monitoraggio.                                                                              |
| inizializzazione            | Inizializzare il nastro (supporti), che comporta la registrazione del timecode (se possibile) per audio e video vuoti. Questo comando può richiedere diverse ore se è necessario inizializzare l'intero nastro.                                                                                                                            |
| insert                | Specifica che i nuovi dati vengono aggiunti al file nella posizione corrente.                                                                                                                                                                                                                                            |
| overwrite             | Specifica che i nuovi dati sostituiranno i dati nel file.                                                                                                                                                                                                                                                           |
| to *position*         | Specifica una posizione finale per la registrazione. Se il flag "to" non è specificato, il dispositivo registra fino a quando non riceve un comando [di arresto](stop.md) [o sospensione.](pause.md)                                                                                                                                        |
| flusso  video | Specifica il flusso video usato per la registrazione. Se non viene specificato e il formato di file non definisce un valore predefinito, viene registrato nel flusso che viene fisicamente prima.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La registrazione viene arrestata quando viene [eseguito](stop.md) un comando [di](pause.md) arresto o sospensione. Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.

Prima di eseguire comandi che usano valori di posizione, è necessario impostare il formato di ora desiderato usando il [comando set.](set.md) Le tracce da registrare sono specificate dai comandi [settimecode](settimecode.md) "record", "assemble record", [setvideo](setvideo.md) "record" e [setaudio](setaudio.md) "record".

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

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[segnale](cue.md)
</dt> <dt>

[Monitor](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Mettere](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

