---
title: comando capability
description: Il comando capability richiede informazioni su una particolare funzionalità di un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- comando capability Windows Multimedia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e57a793f799214753f50504d80bce7051fba14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469158"
---
# <a name="capability-command"></a>comando capability

Il comando capability richiede informazioni su una particolare funzionalità di un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag che identifica una funzionalità del dispositivo. La tabella seguente elenca i tipi di dispositivo che riconoscono **il comando capability** e i flag usati da ogni tipo:




| valore | Tipo | Tipo | 
|-------|------|------|
| cdaudio | <ul><li>può essere espulso</li><li>può riprodurre</li><li>può registrare</li><li>può salvare</li><li>dispositivo composto</li></ul> | <ul><li>tipo di dispositivo</li><li>dispone di audio</li><li>ha un video</li><li>usa i file</li></ul> | 
| digitalvideo | <ul><li>può essere espulso</li><li>può bloccarsi</li><li>può bloccare</li><li>può riprodurre</li><li>può registrare</li><li>può invertire</li><li>può salvare</li><li>può estendersi</li><li>può estendere l'input</li><li>può testare</li></ul> | <ul><li>dispositivo composto</li><li>tipo di dispositivo</li><li>dispone di audio</li><li>ha ancora</li><li>ha un video</li><li>velocità di riproduzione massima</li><li>frequenza di riproduzione minima</li><li>usa i file</li><li>usa i tavolozze</li><li>windows</li></ul> | 
| overlay | <ul><li>può essere espulso</li><li>può bloccarsi</li><li>può riprodurre</li><li>può registrare</li><li>può salvare</li><li>può estendersi</li></ul> | <ul><li>dispositivo composto</li><li>tipo di dispositivo</li><li>dispone di audio</li><li>ha un video</li><li>usa i file</li><li>windows</li></ul> | 
| sequencer | <ul><li>può essere espulso</li><li>può riprodurre</li><li>può registrare</li><li>può salvare</li><li>dispositivo composto</li></ul> | <ul><li>tipo di dispositivo</li><li>dispone di audio</li><li>ha un video</li><li>usa i file</li></ul> | 
| Vcr | <ul><li>può rilevare la lunghezza</li><li>può essere espulso</li><li>può bloccarsi</li><li>può monitorare le origini</li><li>può riprodurre</li><li>può eseguire la pre-registrazione</li><li>può visualizzare l'anteprima</li><li>può registrare</li><li>può invertire</li><li>può salvare</li><li>può testare</li></ul> | <ul><li>frequenza di incremento dell'orologio</li><li>dispositivo composto</li><li>tipo di dispositivo</li><li>dispone di audio</li><li>ha l'orologio</li><li>ha il codice temporale</li><li>ha un video</li><li>numero di contrassegni</li><li>ricerca dell'accuratezza</li><li>usa i file</li></ul> | 
| videodisc | <ul><li>può essere espulso</li><li>può riprodurre</li><li>può registrare</li><li>può invertire</li><li>può salvare</li><li>CAV</li><li>CLV</li><li>dispositivo composto</li></ul> | <ul><li>tipo di dispositivo</li><li>velocità di riproduzione veloce</li><li>dispone di audio</li><li>ha un video</li><li>velocità di riproduzione normale</li><li>velocità di riproduzione lenta</li><li>usa i file</li></ul> | 
| Waveaudio | <ul><li>può essere espulso</li><li>può riprodurre</li><li>può registrare</li><li>può salvare</li><li>dispositivo composto</li><li>tipo di dispositivo</li></ul> | <ul><li>dispone di audio</li><li>ha un video</li><li>input</li><li>outputs</li><li>usa i file</li></ul> | 




 

La tabella seguente elenca i flag che possono essere specificati nel *parametro lpszRequest* e i relativi significati:




| Flags | Significato | 
|-------|---------|
| può rilevare la lunghezza | Restituisce <strong>TRUE</strong> se il dispositivo è in grado di rilevare la lunghezza del supporto. | 
| può essere espulso | Restituisce <strong>TRUE</strong> se il dispositivo può espulso il supporto. | 
| può bloccarsi | Restituisce <strong>TRUE</strong> se il dispositivo può bloccare i dati nel buffer dei frame. | 
| può bloccare | Restituisce <strong>TRUE se</strong> il dispositivo può bloccare i dati. | 
| può monitorare le origini | Restituisce <strong>TRUE</strong> se il dispositivo può passare un input (origine) all'output monitorato, indipendentemente dalla selezione di input corrente. | 
| può riprodurre | Restituisce <strong>TRUE se</strong> il dispositivo può riprodurre. | 
| può eseguire la pre-registrazione | Restituisce <strong>TRUE</strong> se il dispositivo supporta il flag "preroll" con il <a href="cue.md">comando cue.</a> | 
| può visualizzare in anteprima | Restituisce <strong>TRUE</strong> se il dispositivo supporta le anteprime. | 
| può registrare | Restituisce <strong>TRUE se</strong> il dispositivo supporta la registrazione. | 
| può invertire | Restituisce <strong>TRUE se</strong> il dispositivo può essere riprodotto in ordine inverso. | 
| può salvare | Restituisce <strong>TRUE se</strong> il dispositivo può salvare i dati. | 
| può essere estesa | Restituisce <strong>TRUE se</strong> il dispositivo può estendere i fotogrammi per riempire un rettangolo di visualizzazione specificato. | 
| può estendere l'input | Restituisce <strong>TRUE</strong> se il dispositivo può ridimensionare un'immagine durante il processo di digitalizzazione nel buffer dei frame. | 
| può testare | Restituisce <strong>TRUE se</strong> il dispositivo riconosce la parola chiave test. | 
| Cav | In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano ai videodisc in formato CAV. Questa è l'impostazione predefinita se non viene inserito alcun elemento videodisc. | 
| clock increment rate | Restituisce il numero di suddivisioni supportate al secondo dall'orologio esterno. Se il clock esterno è un clock in millisecondi, il valore restituito è 1000. Se il valore restituito è 0, non è supportato alcun clock. | 
| clv | In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano ai videodisc in formato CLV. | 
| dispositivo composto | Restituisce <strong>TRUE se</strong> il dispositivo supporta un nome di elemento (nome file). | 
| tipo di dispositivo | Restituisce un nome di tipo di dispositivo, che può essere uno dei seguenti:<ul><li>cdaudio</li><li>Dat</li><li>digitalvideo</li><li>altro</li><li>overlay</li><li>scanner</li><li>sequencer</li><li>Vcr</li><li>videodisc</li><li>Waveaudio</li></ul> | 
| velocità di riproduzione veloce | Restituisce la velocità di riproduzione veloce in fotogrammi al secondo oppure zero se il dispositivo non può riprodurre velocemente. | 
| dispone di audio | Restituisce <strong>TRUE se</strong> il dispositivo supporta la riproduzione audio. | 
| ha l'orologio | Restituisce <strong>TRUE</strong> se il dispositivo ha un orologio. | 
| ha ancora | Restituisce <strong>TRUE se</strong> il dispositivo considera i file con una singola immagine in modo più efficiente rispetto ai file video in movimento. | 
| ha timecode | Restituisce <strong>TRUE</strong> se il dispositivo è in grado di supportare il timecode o se è sconosciuto. | 
| ha un video | Restituisce <strong>TRUE</strong> se il dispositivo supporta video. | 
| input | Restituisce il numero totale di dispositivi di input. | 
| velocità di riproduzione massima | Restituisce la velocità di riproduzione massima, in fotogrammi al secondo, per il dispositivo. | 
| velocità di riproduzione minima | Restituisce la velocità di riproduzione minima, in fotogrammi al secondo, per il dispositivo. | 
| velocità di riproduzione normale | Restituisce la velocità di riproduzione normale, in fotogrammi al secondo, per il dispositivo. | 
| numero di contrassegni | Restituisce il numero massimo di contrassegni che è possibile utilizzare. zero indica che i contrassegni non sono supportati. | 
| outputs | Restituisce il numero totale di dispositivi di output. | 
| ricerca dell'accuratezza | Restituisce l'accuratezza prevista di una ricerca in frame. 0 indica che il dispositivo è preciso per il frame, 1 indica che il dispositivo si aspetta di essere all'interno di un frame della posizione di ricerca indicata e così via. | 
| velocità di riproduzione lenta | Restituisce la velocità di riproduzione lenta in fotogrammi al secondo oppure zero se il dispositivo non può essere riprodotto lentamente. | 
| usa i file | Restituisce <strong>TRUE se</strong> l'archivio dati usato da un dispositivo composto è un file. | 
| usa i tavolozze | Restituisce <strong>TRUE</strong> se il dispositivo usa i tavolozze. | 
| windows | Restituisce il numero di finestre di visualizzazione simultanee supportate dal dispositivo. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce informazioni nel *parametro lpszReturnString* della [**funzione mciSendString.**](/previous-versions//dd757161(v=vs.85)) Le informazioni dipendono dal tipo di richiesta.

## <a name="examples"></a>Esempio

Il comando seguente restituisce il tipo di dispositivo del dispositivo "mysound".

``` syntax
capability mysound device type
```

## <a name="requirements"></a>Requisiti



| Requisito | valore |
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
</dt> </dl>

 

