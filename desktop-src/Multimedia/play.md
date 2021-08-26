---
title: comando play
description: Il comando play avvia la riproduzione di un dispositivo. Questo comando viene riconosciuto da cd audio, digital-video, sequencer MIDI, videodisc, vcr e waveform-audio.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- Comando play Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da0df530f1c7a0166dcbb7c852fe491127a9e187d1cb6cb953ec46b2533ac00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038051"
---
# <a name="play-command"></a>comando play

Il comando play avvia la riproduzione di un dispositivo. Questo comando viene riconosciuto da cd audio, digital-video, sequencer MIDI, videodisc, vcr e waveform-audio.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Flag per la riproduzione di un dispositivo. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando play** e i flag usati da ogni tipo.



| Valore        | Significato                          | Significato                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | dalla *posizione*                  | alla *posizione*                     |
| digitalvideo | dalla *ripetizione* a schermo intero della posizione | finestra inversa *alla* posizione       |
| sequencer    | dalla *posizione*                  | alla *posizione*                     |
| Vcr          | al *momento dalla* posizione *inversa*  | eseguire l'analisi in *posizione*                |
| videodisc    | veloce *dall'analisi inversa* della posizione | numero intero a *velocità lenta* da *posizionare* |
| Waveaudio    | dalla *posizione*                  | alla *posizione*                     |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszPlayFlags** e i relativi significati.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alla *volta*       | Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato indicato, quando inizia il comando cued. Per altre informazioni, vedere il [comando cue.](cue.md)                                                                                                                                                                                                                                                                 |
| veloce            | Indica che il dispositivo deve essere riprodotto più velocemente del normale. Per determinare la velocità esatta di un lettore videodisc, usare il flag "speed" del [comando status.](status.md) Per specificare la velocità in modo più preciso, usare il flag "speed" di questo comando.                                                                                                                                                                                                   |
| dalla *posizione* | Specifica una posizione iniziale per la riproduzione. Se il flag "from" non è specificato, la riproduzione inizia nella posizione corrente. Per **i dispositivi cdaudio,** se la posizione "da" è maggiore della posizione finale del disco o se la posizione "da" è maggiore della posizione "a", il driver restituisce un errore. Per **i dispositivi videodisc,** le posizioni predefinite sono in fotogrammi per i dischi CAV e in ore, minuti e secondi per i dischi CLV. |
| Fullscreen      | Specifica che deve essere usata una visualizzazione a schermo intero. Usare questo flag solo durante la riproduzione di file compressi. I file non compressi non vengono riprodotti a schermo intero.                                                                                                                                                                                                                                                                                                  |
| ripetere          | Specifica che la riproduzione deve essere riavviata quando viene raggiunta la fine del contenuto.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Specifica che la direzione di riproduzione è all'indietro. Non è possibile specificare una posizione finale con il flag "reverse". Per i videodisc, la "scansione" si applica solo al formato CAV.                                                                                                                                                                                                                                                                                     |
| Scansione            | Viene riprodotto il più velocemente possibile senza disabilitare il video (anche se l'audio potrebbe essere disabilitato). Per i videodisc, la "scansione" si applica solo al formato CAV.                                                                                                                                                                                                                                                                                                             |
| lento            | Viene riprodotto lentamente. Per determinare la velocità esatta di un lettore videodisc, usare il flag "speed" del [comando status.](status.md) Per specificare la velocità in modo più preciso, usare il flag "speed" di questo comando. Per i videodisc, "slow" si applica solo al formato CAV.                                                                                                                                                                                            |
| speed *integer* | Riproduce un videodisc alla velocità specificata, in fotogrammi al secondo. Questo flag si applica solo ai dischi CAV.                                                                                                                                                                                                                                                                                                                                                 |
| alla *posizione*   | Specifica una posizione finale per la riproduzione. Se il flag "to" non è specificato, la riproduzione viene interrotta alla fine del contenuto. Per **i dispositivi cdaudio,** se la posizione "a" è maggiore della posizione finale del disco, il driver restituisce un errore. Per **i dispositivi videodisc,** le posizioni predefinite sono in fotogrammi per i dischi CAV e in ore, minuti e secondi per i dischi CLV.                                                                  |
| Finestra          | Specifica che la riproduzione deve usare la finestra associata all'istanza del dispositivo. Si tratta dell'impostazione predefinita.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Prima di eseguire comandi che usano valori di posizione, è necessario impostare il formato ora desiderato usando il [comando set.](set.md) Questo comando inizia a essere riprodotto alla velocità corrente, come impostato con il comando set "speed". La direzione è inversa se viene specificato il flag "reverse" o se il flag "to" viene specificato come valore minore del flag "from". Se il flag "from" non è specificato, la riproduzione inizia nella posizione corrente. I flag "to" e "reverse" non possono essere usati insieme.

## <a name="examples"></a>Esempio

Il comando seguente riproduce il dispositivo "mysound" dalla posizione 1000 alla posizione 2000, inviando un messaggio di notifica al termine della riproduzione.

``` syntax
play mysound from 1000 to 2000 notify
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

[set](set.md)
</dt> </dl>

 

