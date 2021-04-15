---
title: comando seek
description: Il comando Seek passa alla posizione specificata e si arresta. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- comando Cerca Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400257"
---
# <a name="seek-command"></a>comando seek

Il comando Seek passa alla posizione specificata e si arresta. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

Flag per lo stato di passaggio a una posizione specificata. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Seek** e i flag utilizzati da ogni tipo.



| Valore        | Significato                          | Significato                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | per terminare la *posizione*             | per iniziare                     |
| digitalvideo | per terminare la *posizione*             | per iniziare                     |
| sequencer    | per terminare la *posizione*             | per iniziare                     |
| VCR          | al *segno* di *spunta \_ num* | per terminare la *posizione* iniziale |
| videodisco    | Inverti alla fine                   | per *posizionare* l'avvio        |
| WaveAudio    | per terminare la *posizione*             | per iniziare                     |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszSeekFlags** e i relativi significati.



| Valore            | Significato                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *momento*        | Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando. Per ulteriori informazioni, vedere il comando [cue](cue.md) .                             |
| segno *di \_ spunta* | Cerca il contrassegno relativo indicato da *Mark \_ num*, che deve essere un valore intero positivo. I contrassegni sono segnali scritti sul nastro VCR usando il comando [Mark](mark.md) e vengono usati per la ricerca ad alta velocità. |
| reverse          | Indica che la direzione di ricerca nei VCR e videodischi CAV è precedente. Questo flag non è valido se è specificato il flag "to". Per i VCR, questo flag deve essere usato con il flag "Mark".                             |
| alla fine           | Cerca alla fine del contenuto.                                                                                                                                                                                 |
| *posizione*    | Specifica la posizione in cui arrestare la ricerca. Per i dispositivi **CDAudio** , MCI restituisce un errore non compreso nell'intervallo se la posizione specificata è maggiore della lunghezza del disco.                                            |
| per iniziare         | Cerca l'inizio del contenuto.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .

I dispositivi digitali video supportano due modalità di ricerca, che è possibile modificare usando il comando [imposta](set.md) . La modalità "seek exactly on" causa il passaggio del comando seek al frame specificato. La modalità "seek exactly off" causa il passaggio del comando seek al fotogramma chiave più vicino prima del frame specificato.

Se un dispositivo audio CD viene riprodotto quando viene emesso il comando seek, la riproduzione viene arrestata. Quando il comando Seek viene emesso con un dispositivo videodisco, il dispositivo esegue la ricerca con l'opzione di avanzamento rapido o veloce con audio e video.

Quando il comando Seek viene emesso con un dispositivo audio Waveform, il comportamento dipende dalle dimensioni del campione. Se le dimensioni del campione sono pari o superiori a 16 bit, Seek si sposta all'inizio dell'esempio più vicino quando una posizione specificata non coincide con l'inizio di un campione.

## <a name="examples"></a>Esempio

Il comando seguente consente di cercare l'inizio del file multimediale associato al dispositivo "audio".

``` syntax
seek mysound to start
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

[contrassegnare](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

