---
title: Comando setvideo
description: Il comando setvideo imposta i valori associati alla riproduzione e all'acquisizione di video. I dispositivi video e videoregistratori digitali riconoscono questo comando.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- Comando setvideo Windows Multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674b8b35c21fa54f1c2ecfc8b9dff531266c319b827d675da46be04e6c7abe8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805381"
---
# <a name="setvideo-command"></a>Comando setvideo

Il comando setvideo imposta i valori associati alla riproduzione e all'acquisizione di video. I dispositivi video e videoregistratori digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Contrassegnare per la riproduzione e l'acquisizione di video. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando setvideo** e i flag usati da ogni tipo.



| Valore        | Significato                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | algoritmo *bitsperpel* per contare la luminosità a *fattore* clocktimecolor per fattore contrasto al fattore gamma al valore halftoneinputkey color to *r:g:b* key index to *index* offonoutput     | su duration palette *color* over *index* to *newrgb* palette handle to *handle* quality *descriptor* record frame rate to rate *record* onrecord offsharpness to *factor* source to *source* *number* value still quality *descriptor* stream to *number* tint to *factor* |
| Vcr          | offonmonitor per digitare *number* *number* record offrecord track *track \_ number* off                                                                                                               | record onrecord track *track \_ number* onsource to *type* *number* track *\_ number* offtrack *track \_ number* on                                                                                                                                                                             |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszVideo** e i relativi significati.



| Valore                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo *algoritmo*                          | Specifica un algoritmo di compressione video per l'uso da parte di un comando [reserve o](reserve.md) [record](record.md) successivo. Gli algoritmi supportati da un dispositivo sono specifici del dispositivo. MCI definisce le costanti "mpeg" e "h261" per *l'algoritmo*. Se l'algoritmo specificato è in conflitto con il formato di file corrente, il formato di file viene modificato nel formato predefinito per l'algoritmo.<br/>                                                                                                                                     |
| bitsperpel da *contare*                          | Imposta il numero di bit per pixel per il salvataggio dei dati con il [comando capture](capture.md) [o record.](record.md)                                                                                                                                                                                                                                                                                                                                                                                                              |
| luminosità a *fattore*                         | Imposta il livello di luminosità del video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Indica che il tempo specificato nel flag "over" è espresso in millisecondi. Il tempo è assoluto e non al passo con la riproduzione dell'area di lavoro.                                                                                                                                                                                                                                                                                                                                                                                |
| da colore a *fattore*                              | Imposta il livello di saturazione dei colori.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contrasto al *fattore*                           | Imposta il livello di contrasto video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gamma al *valore*                               | Specifica l'esponente di correzione gamma moltiplicato per 1000. Ad esempio, per specificare un esponente di 2.2, usare 2200 per *il valore*. Un valore gamma pari a 1,0 (1000) indica che non viene applicata alcuna correzione gamma. Correzione gamma regola il mapping tra l'intensità codificata nell'origine della presentazione e la luminosità visualizzata.                                                                                                                                                                                                 |
| Semitono                                       | Fa sì che il riquadro dei mezzitoni sia usato anziché il riquadro predefinito. Questo flag è riconosciuto solo dal driver video digitale MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Modifica il flag "brightness", "color", "contrast", "gamma", "sharpness" o "tint" in modo che influisca sul segnale di input e modifichi ciò che viene registrato. Se possibile, si tratta dell'impostazione predefinita quando si monitora l'input.                                                                                                                                                                                                                                                                                                             |
| colore chiave *per r:g:b*                           | Imposta il colore della chiave. La *variabile r:g:b* è un valore RGB. Due punti (:) separare i singoli valori rosso, verde e blu.                                                                                                                                                                                                                                                                                                                                                                                                       |
| indice della chiave da *indicizzare*                           | Imposta l'indice della chiave. La *variabile di* indice è un indice del riquadro fisico.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| monitor per  *digitare il numero*              | Controlla l'input di origine che verrà passato all'output del videoregistratore, senza modificare la selezione dell'input dell'origine di registrazione. Il tipo può essere "output" o una delle origini di input valide. Se "number" non viene specificato, viene scelto il primo input di tale tipo.                                                                                                                                                                                                                                                                        |
| offon                                          | Abilita o disabilita la visualizzazione del video. La disabilitazione del video imposta i pixel nel rettangolo [put](put.md) "destination" (o l'area client predefinita della finestra corrente) su un colore a tinta unita. Non ha alcun effetto sul buffer dei frame. L'origine video, che sia l'area di lavoro o un input esterno, potrebbe continuare a archiviare nuove immagini nel buffer dei fotogrammi. Non vengono visualizzate fino a quando non viene abilitato il video. È possibile usare il [comando](window.md) "state" della finestra per nascondere la finestra. Il valore predefinito **è setvideo** "on".<br/> |
| output                                         | Modifica il flag "brightness", "color", "contrast", "gamma", "sharpness" o "tint" in modo che modifichi solo il segnale visualizzato e non ciò che viene registrato. Se possibile, si tratta dell'impostazione predefinita quando si monitora un file.                                                                                                                                                                                                                                                                                                           |
| nel corso della *durata*                                | Specifica il tempo necessario per apportare una modifica che usa una *variabile fattore.* Le unità per *la durata* sono nel formato di ora corrente. Le modifiche si verificano nel passaggio con la riproduzione dell'area di lavoro. Quando la riproduzione viene sospesa, anche la modifica viene sospesa fino a quando la riproduzione non continua. Se "over" non viene usato o non è supportato, la modifica si verifica immediatamente.                                                                                                                                                                    |
| Colore della *tavolozza rispetto* *all'indice* in *newrgb* | Imposta un nuovo colore della tavolozza. L'indice del colore e della tavolozza da modificare viene specificato dai parametri *color* *e index.* il nuovo colore viene specificato da *newrgb*. Questo flag è riconosciuto solo dal driver video digitale MCIAVI.                                                                                                                                                                                                                                                                                               |
| Handle del riquadro da *gestire*                     | Specifica l'handle per una tavolozza che il dispositivo deve usare per il rendering. Questo elemento è supportato solo dai dispositivi che usano i palette. Se *handle* è zero, viene usato il riquadro predefinito. I dispositivi digital-video non devono liberare la tavolozza passata con questo comando. Le applicazioni devono liberarlo dopo la chiusura del dispositivo.<br/>                                                                                                                                                                                                 |
| Descrittore *di qualità*                           | Specifica le caratteristiche della compressione video eseguita quando il video viene registrato in un file. Tutti i dispositivi supportano i tre descrittori: "low", "medium" e "high". Il valore predefinito è specifico del dispositivo. Il significato di questi nomi dipende dall'algoritmo e dal dispositivo. I dispositivi possono definire nomi di descrittori aggiuntivi. Il [comando quality](quality.md) può essere usato per definire nomi di descrittori aggiuntivi. Se il flag "algorithm" non viene usato, il *descrittore* si applica all'algoritmo corrente.<br/>   |
| frequenza fotogrammi record per la *frequenza*                    | Imposta la registrazione per il video in movimento. La velocità *di* registrazione è specificata in unità di fotogrammi al secondo moltiplicate per 1000. Ad esempio, la frequenza dei fotogrammi NTSC di 29,97 fotogrammi al secondo è rappresentata come 29970.                                                                                                                                                                                                                                                                                                                   |
| record onrecord off                            | Abilita o disabilita la registrazione dei dati video. La registrazione dei dati video è l'impostazione predefinita.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| registrare track *track \_ number* off               | Cancella la selezione dell'origine video in modo che nessun video verrà registrato con il comando [di record](record.md) successivo. "Track" consente la selezione di tracce indipendenti. Se "track" non viene specificato, viene utilizzato il valore predefinito 1. Potrebbe essere necessario eseguire prima un [comando set](set.md) "assemble record off" prima di poter disattivare la registrazione video.                                                                                                                                                                     |
| registrare il *numero di \_ traccia* su                | Seleziona l'origine video da registrare con il comando **di registrazione** successivo. "Track" consente la selezione di tracce indipendenti. La traccia 2 corrisponde alla traccia PCM in Hi8. Se "track" non viene specificato, viene utilizzato il valore predefinito 1.                                                                                                                                                                                                                                                                                                      |
| nitidezza da *fattore a fattore*                          | Imposta il livello di nitidezza video.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Valore del numero da origine *a* *origine*              | Imposta l'origine dell'input video. In genere corrisponde a connettori esterni. Le costanti definite per *source* includono "rgb", "pal", "ntsc", "svideo" e "secam". Se sono presenti più input del tipo specificato,  il valore facoltativo "number" indica l'input desiderato. Ad esempio, **setvideo** "source to ntsc number 2" specifica il secondo input NTSC. Se *l'origine* "to" viene omessa, l'origine assoluta viene usata come definito dal comando [list](list.md) "video source".<br/>            |
| source per *digitare il* numero *numero*               | Seleziona l'origine video da registrare sul nastro. *Il* tipo deve essere "tuner", "line", "svideo", "aux", "generic", "mute" o "rgb".                                                                                                                                                                                                                                                                                                                                                                                              |
| algoritmo  still                    | Specifica l'algoritmo di compressione dell'immagine ancora usato dal [comando di](capture.md) acquisizione. Ogni dispositivo deve supportare un *algoritmo* "none", ovvero nessuna compressione. Questo è il valore predefinito. In questo caso, i dispositivi video digitali salvano le immagini fisse come bitmap RGB indipendenti dal dispositivo. I dispositivi possono anche supportare un elenco specifico del dispositivo di algoritmi aggiuntivi.                                                                                                                                                           |
| descrittore di *qualità ancora*                     | Specifica le caratteristiche della compressione dell'immagine ancorata eseguita durante l'acquisizione di un'immagine. Tutti i dispositivi supportano i descrittori "low", "medium" e "high". Il valore predefinito è specifico del dispositivo. Se il flag "algorithm" non viene usato, il *descrittore* si applica all'algoritmo corrente.<br/> Il [comando quality](quality.md) può essere usato per definire altri nomi di descrittori.<br/>                                                                                                                            |
| da flusso a *numero*                             | Specifica il flusso video riprodotto dall'area di lavoro. Se il flusso non è specificato e un flusso predefinito non è definito dal formato di file, viene riprodotto il primo flusso video interleaved fisicamente.                                                                                                                                                                                                                                                                                                                 |
| tinta da *fattore*                               | Imposta la tinta dell'immagine. In genere, questa regolazione viene modellata in base al controllo della tinta di molti set di tv a colori, con 250 che significa verde, 750 che significa rosso e 0 (o                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Per i dispositivi VCR, l'uso di setvideo con un flag che disattiva una singola traccia ("track *track \_ number* off") potrebbe causare la ricezione di un messaggio di stato che indica che non è stato possibile eseguire il comando. Alcuni videoregistratori possono disattivare solo combinazioni di tracce, non singole tracce; ad esempio la prima traccia audio e una traccia video di una cassetta video. In questo caso, è sufficiente [usare setaudio](setaudio.md) e setvideo per continuare a disattivare le altre tracce che costituiscono la combinazione. Il driver disattiva le tracce quando riceve il comando per disattivare l'ultima traccia nella combinazione.

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

[Catturare](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[Mettere](put.md)
</dt> <dt>

[Registrazione](record.md)
</dt> <dt>

[Riserva](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[Finestra](window.md)
</dt> </dl>

 

