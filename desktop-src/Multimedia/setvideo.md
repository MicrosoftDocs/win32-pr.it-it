---
title: comando sevideo
description: Il comando sevideo imposta i valori associati alla riproduzione video e all'acquisizione. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- comando sevideo Windows Multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa4c3d1e3b90b9ab0c5bf5791dacd541c8a8bc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400715"
---
# <a name="setvideo-command"></a>comando sevideo

Il comando sevideo imposta i valori associati alla riproduzione video e all'acquisizione. I dispositivi Digital-video e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("setvideo %s %s %s"), 
  lpszDeviceID, 
  lpszVideo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Flag per la riproduzione e l'acquisizione di video. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **sevideo** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | algoritmo *dell'algoritmo BitsPerPel per* il *conteggio* della luminosità al *fattore* di clocktimecolor per *il fattore di differenza tra* il *fattore gamma e* il *valore* halftoneinputkey e *r:g: b* indice chiave per l' *indicizzazione* offonoutput | over *Duration* tavolozza *colore colore sopra* *Indice* all'handle della tavolozza *newrgb* per *gestire* la frequenza dei fotogrammi dei record del *descrittore* per *valutare* il record onrecord offsharpness per *fattorizzare* l'origine al *valore* del *numero di* *origine* ancora *algoritmo* algoritmo algoritmo ancora la qualità flusso del *descrittore* del *numero* |
| VCR          | offonmonitor al *tipo* di *numero di record offrecord* Track *Track \_ Number* off                                                                                                               | registrare il *\_ numero* di track track del record onsource nel *tipo* *numero di* *traccia numero di traccia clandestine numero \_* di traccia su *\_*                                                                                                                                                                             |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszVideo** e i relativi significati.



| Valore                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo *algoritmo*                          | Specifica un algoritmo di compressione video per l'uso da un comando [Reserve](reserve.md) o [record](record.md) successivo. Gli algoritmi supportati da un dispositivo sono specifici del dispositivo. MCI definisce le costanti "MPEG" e "H261" per l' *algoritmo*. Se l'algoritmo specificato è in conflitto con il formato di file corrente, il formato del file viene modificato nel formato predefinito per l'algoritmo.<br/>                                                                                                                                     |
| BitsPerPel da *contare*                          | Imposta il numero di bit per pixel per il salvataggio dei dati con il comando [Capture](capture.md) o [record](record.md) .                                                                                                                                                                                                                                                                                                                                                                                                              |
| luminosità a *fattore*                         | Imposta il livello di luminosità del video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Indica che l'ora specificata nel flag "over" è in millisecondi. Il tempo è assoluto e non in fase di riproduzione dell'area di lavoro.                                                                                                                                                                                                                                                                                                                                                                                |
| da colore a *fattore*                              | Imposta il livello di saturazione del colore.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contrasto con il *fattore*                           | Imposta il livello di contrasto del video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| da gamma a *valore*                               | Specifica l'esponente di correzione gamma moltiplicato per 1000. Per specificare, ad esempio, un esponente di 2,2, utilizzare 2200 per *valore*. Un valore gamma di 1,0 (1000) indica che non viene applicata alcuna correzione gamma. La correzione gamma regola il mapping tra l'intensità codificata nell'origine della presentazione e la luminosità visualizzata.                                                                                                                                                                                                 |
| mezzitoni                                       | Consente di utilizzare la tavolozza dei mezzitoni al posto della tavolozza predefinita. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Modifica il flag "luminosità", "colore", "contrasto", "gamma", "nitidezza" o "tinta" in modo che influisca sul segnale di input e modifichi gli elementi registrati. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.                                                                                                                                                                                                                                                                                                             |
| colore della chiave per *r:g: b*                           | Imposta il colore della chiave. La variabile *r:g: b* è un valore RGB. Due punti (:) separare i singoli valori rosso, verde e blu.                                                                                                                                                                                                                                                                                                                                                                                                       |
| indice chiave da *indicizzare*                           | Imposta l'indice della chiave. La variabile di *Indice* è un indice della tavolozza fisica.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *tipo* di monitoraggio per *il numero di serie*              | Controlla quale input di origine verrà passato all'output del VCR, senza modificare la selezione dell'input di origine della registrazione. Il tipo può essere "output" o una delle origini di input valide. Se non si specifica "Number", viene scelto il primo input di quel tipo.                                                                                                                                                                                                                                                                        |
| dimettereun                                          | Abilita o Disabilita la visualizzazione del video. La disabilitazione del video imposta i pixel nel rettangolo [put](put.md) "Destination" (o il relativo valore predefinito, l'area client della finestra corrente) su un colore a tinta unita. Non ha alcun effetto sul buffer dei frame. L'origine video, sia che si tratti di un'area di lavoro o di un input esterno, potrebbe continuare a archiviare nuove immagini nel buffer dei frame. Non vengono visualizzate finché il video non è abilitato. È possibile utilizzare il comando "stato" della [finestra](window.md) per nascondere la finestra. Il valore predefinito è **sevideo** "on".<br/> |
| output                                         | Modifica il flag "luminosità", "colore", "contrasto", "gamma", "nitidezza" o "tinta" in modo che modifichi solo il segnale visualizzato e non quello registrato. Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio di un file.                                                                                                                                                                                                                                                                                                           |
| oltre la *durata*                                | Specifica il tempo necessario per apportare una modifica che usa una variabile di *fattore* . Le unità per la *durata* sono nel formato di ora corrente. Le modifiche vengono eseguite nel passaggio con la riproduzione dell'area di lavoro. Quando la riproduzione viene sospesa, la modifica viene sospesa anche fino a quando non continua la riproduzione. Se "over" non viene usato o non è supportato, la modifica viene eseguita immediatamente.                                                                                                                                                                    |
| *colore* colore tavolozza sull' *Indice* per *newrgb* | Imposta un nuovo colore della tavolozza. Il colore e l'indice della tavolozza da modificare vengono specificati dai parametri *color* e *index* ; il nuovo colore viene specificato da *newrgb*. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.                                                                                                                                                                                                                                                                                               |
| handle tavolozza da *gestire*                     | Specifica l'handle per una tavolozza che il dispositivo deve usare per il rendering. Questo elemento è supportato solo dai dispositivi che utilizzano tavolozze. Se *handle* è zero, viene utilizzata la tavolozza predefinita. I dispositivi digitali video non devono liberare la tavolozza passata con questo comando. Le applicazioni devono liberarsi dopo la chiusura del dispositivo.<br/>                                                                                                                                                                                                 |
| *descrittore* qualità                           | Specifica le caratteristiche della compressione video eseguita quando il video viene registrato in un file. Tutti i dispositivi supportano i tre descrittori: "low", "medium" e "High". Il valore predefinito è specifico del dispositivo. Il significato di questi nomi dipende dall'algoritmo e dal dispositivo. I dispositivi potrebbero definire nomi di descrittori aggiuntivi. Il comando [Quality](quality.md) può essere usato per definire nomi di descrittori aggiuntivi. Se il flag "Algorithm" non viene utilizzato, il *descrittore* si applica all'algoritmo corrente.<br/>   |
| frequenza del frame di record per la *frequenza*                    | Imposta la registrazione per il video di movimento. La *velocità* di registrazione viene specificata in unità di fotogrammi al secondo moltiplicato per 1000. Ad esempio, la frequenza dei fotogrammi NTSC di 29,97 fotogrammi al secondo viene rappresentata come 29970.                                                                                                                                                                                                                                                                                                                   |
| record onrecord off                            | Abilita o Disabilita la registrazione dei dati video. La registrazione dei dati video è il valore predefinito.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| registrare il *\_ numero* di Track Track               | Cancella la selezione dell'origine video in modo che nessun video venga registrato con il comando [record](record.md) successivo. "Track" consente la selezione di tracce indipendente. Se "Track" non è specificato, viene utilizzato il valore predefinito 1. Potrebbe essere necessario prima emettere un [set](set.md) di comandi "assembla record off" prima che la registrazione video possa essere disattivata.                                                                                                                                                                     |
| registra il *\_ numero di traccia* su                | Consente di selezionare l'origine video da registrare con il comando **record** successivo. "Track" consente la selezione di tracce indipendente. Track 2 corrisponde alla traccia PCM in Hi8. Se non si specifica "Track", verrà utilizzato il valore predefinito 1.                                                                                                                                                                                                                                                                                                      |
| nitidezza a *fattore*                          | Imposta il livello di nitidezza del video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| da origine a *valore* numero di *origine*              | Imposta l'origine dell'input video. Corrisponde in genere a connettori esterni. Le costanti definite per l' *origine* includono "RGB", "PAL", "NTSC", "SVIDEO" e "SECAM". Se esiste più di un input del tipo specificato, il *valore* "Number" facoltativo indica l'input desiderato. Ad esempio, **sevideo** "source to NTSC numero 2" specifica il secondo input NTSC. Se l' *origine* "to" viene omessa, l'origine assoluta viene usata come definito dal comando [List](list.md) "video source".<br/>            |
| da origine a *numero* di *tipo*               | Consente di selezionare l'origine video da registrare sul nastro. Il *tipo* deve essere "Tuner", "line", "SVIDEO", "aux", "Generic", "mute" o "RGB".                                                                                                                                                                                                                                                                                                                                                                                              |
| *algoritmo* di algoritmo ancora                    | Specifica l'algoritmo di compressione delle immagini ancora utilizzato dal comando di [acquisizione](capture.md) . Ogni dispositivo deve supportare un *algoritmo* di "None", che significa nessuna compressione. Questo è il valore predefinito. In questo caso, i dispositivi digitali video salvano le immagini ancora come bitmap indipendenti dal dispositivo RGB. I dispositivi possono inoltre supportare un elenco specifico del dispositivo di algoritmi aggiuntivi.                                                                                                                                                           |
| *descrittore* di qualità ancora                     | Specifica le caratteristiche della compressione Still-Image eseguita durante l'acquisizione di un'immagine ancora. Tutti i dispositivi supportano i descrittori "low", "medium" e "High". Il valore predefinito è specifico del dispositivo. Se il flag "Algorithm" non viene utilizzato, il *descrittore* si applica all'algoritmo corrente.<br/> Il comando [Quality](quality.md) può essere usato per definire altri nomi di descrittori.<br/>                                                                                                                            |
| da flusso a *numero*                             | Specifica il flusso video riprodotto dall'area di lavoro. Se il flusso non è specificato e un flusso predefinito non è definito dal formato di file, viene riprodotto il primo flusso video interleaved fisicamente.                                                                                                                                                                                                                                                                                                                 |
| tinta per *fattore*                               | Imposta la tinta dell'immagine. In genere, questa regolazione viene modellata dopo il controllo della tinta di molti set di televisori colore, con 250 significa verde, 750 che significa rosso e 0 (o                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per i dispositivi VCR, l'uso di sevideo con un flag che disattiva una singola traccia ("Track *Track \_ Number* off") può causare la ricezione di un messaggio di stato da parte dell'applicazione che indica che non è stato possibile eseguire il comando. Alcuni VCR possono disattivare solo le combinazioni di tracce, non le singole tracce; ad esempio, la prima traccia audio e una traccia video di una cassetta video. In questo caso, è sufficiente utilizzare l'opzione [seaudio](setaudio.md) e sevideo per continuare a disattivare le altre tracce che compongono la combinazione. Il driver disattiva le tracce quando riceve il comando per disattivare l'ultima traccia della combinazione.

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

[catturare](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[mettere](put.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[riserva](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[finestra](window.md)
</dt> </dl>

 

