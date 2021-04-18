---
title: comando Play
description: Il comando Play avvia la riproduzione di un dispositivo. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- comando Riproduci Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301372"
---
# <a name="play-command"></a>comando Play

Il comando Play avvia la riproduzione di un dispositivo. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Flag per la riproduzione di un dispositivo. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Play** e i flag utilizzati da ogni tipo.



| Valore        | Significato                          | Significato                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | dalla *posizione*                  | *posizione*                     |
| digitalvideo | dalla *posizione* di ripetizione a schermo intero | Inverti alla finestra *posizione*       |
| sequencer    | dalla *posizione*                  | *posizione*                     |
| VCR          | al *momento* dalla *posizione* inversa  | analizza in *posizione*                |
| videodisco    | analisi inversa rapida dalla *posizione* | velocità *intera* lenta nella *posizione* |
| WaveAudio    | dalla *posizione*                  | *posizione*                     |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszPlayFlags** e i relativi significati.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *momento*       | Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando. Per ulteriori informazioni, vedere il comando [cue](cue.md) .                                                                                                                                                                                                                                                                 |
| veloce            | Indica che il dispositivo deve essere riprodotto più velocemente del normale. Per determinare la velocità esatta in un lettore videodisco, usare il flag "Speed" del comando [status](status.md) . Per specificare la velocità più precisa, usare il flag "Speed" del comando.                                                                                                                                                                                                   |
| dalla *posizione* | Specifica una posizione iniziale per la riproduzione. Se il flag "from" non è specificato, la riproduzione inizia in corrispondenza della posizione corrente. Per i dispositivi **CDAudio** , se la posizione "da" è maggiore della posizione finale del disco o se la posizione "da" è maggiore della posizione "a", il driver restituisce un errore. Per i dispositivi **videodisco** , le posizioni predefinite sono in frame per i dischi CAV e in ore, minuti e secondi per i dischi CLV. |
| schermo intero      | Specifica che deve essere utilizzata una visualizzazione a schermo intero. Utilizzare questo flag solo per la riproduzione di file compressi. I file non compressi non verranno riprodotti a schermo intero.                                                                                                                                                                                                                                                                                                  |
| ripetere          | Specifica che la riproduzione deve essere riavviata quando viene raggiunta la fine del contenuto.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Specifica che la direzione della riproduzione è precedente. Non è possibile specificare un percorso finale con il flag "Reverse". Per videodischi, "Scan" si applica solo al formato CAV.                                                                                                                                                                                                                                                                                     |
| scansione            | Riproduce il più rapidamente possibile senza disabilitare i video (anche se l'audio potrebbe essere disabilitato). Per videodischi, "Scan" si applica solo al formato CAV.                                                                                                                                                                                                                                                                                                             |
| lento            | Viene riprodotto lentamente. Per determinare la velocità esatta in un lettore videodisco, usare il flag "Speed" del comando [status](status.md) . Per specificare la velocità più precisa, usare il flag "Speed" del comando. Per videodischi, "Slow" si applica solo al formato CAV.                                                                                                                                                                                            |
| velocità *Integer* | Riproduce un videodisco alla velocità specificata, in frame al secondo. Questo flag si applica solo ai dischi CAV.                                                                                                                                                                                                                                                                                                                                                 |
| *posizione*   | Specifica una posizione finale per la riproduzione. Se il flag "to" non è specificato, la riproduzione si interrompe alla fine del contenuto. Per i dispositivi **CDAudio** , se la posizione "a" è maggiore della posizione finale del disco, il driver restituisce un errore. Per i dispositivi **videodisco** , le posizioni predefinite sono in frame per i dischi CAV e in ore, minuti e secondi per i dischi CLV.                                                                  |
| Finestra          | Specifica che la riproduzione deve usare la finestra associata all'istanza del dispositivo. Si tratta dell'impostazione predefinita.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Prima di emettere comandi che usano valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) . Questo comando inizia la riproduzione alla velocità corrente, come impostato con il comando set "Speed". La direzione è inversa se viene specificato il flag "Reverse" o se il flag "to" viene specificato come valore minore del flag "from". Se il flag "from" non è specificato, la riproduzione inizia in corrispondenza della posizione corrente. Impossibile utilizzare contemporaneamente i flag "to" e "Reverse".

## <a name="examples"></a>Esempio

Il comando seguente riproduce il dispositivo "audio" dalla posizione 1000 alla posizione 2000, inviando un messaggio di notifica al termine della riproduzione.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[segnale](cue.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

