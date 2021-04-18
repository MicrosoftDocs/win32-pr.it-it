---
title: Elemento EVENT (WMP SDK)
description: L'elemento EVENT definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script contrassegnato come un evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Finestra degli elementi evento Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324992"
---
# <a name="event-element"></a>Elemento EVENT

L'elemento **Event** definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script contrassegnato come un evento.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Attributi

**Nome** (obbligatorio)

Nome dell'evento.

**WHENDONE** (obbligatorio)

Valore che definisce la funzione di Windows Media Player dopo la riproduzione del contenuto A cui si fa riferimento.

Sono possibili i valori seguenti.



| Valore  | Descrizione                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | La voce corrente (il clip interrotto dall'evento) riprende la riproduzione. Se il contenuto è archiviato, riprende nello stesso punto in cui è stato interrotto; Se il contenuto è trasmesso, riprende nella posizione corrente.        |
| NEXT   | L'elemento **entry** successivo viene riprodotto come se l'evento non si fosse verificato e Windows Media Player avesse raggiunto la fine della clip corrente.                                                                                             |
| BREAK  | Se la voce corrente si trova all'interno di un ciclo di **ripetizione** , il ciclo termina come se il numero di ripetizioni fosse stato completato. In caso contrario, Windows Media Player passa alla fine della playlist come se la voce finale fosse stata completata come di consueto. |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                |
|-----------------|-------------------------|
| Elementi padre | **ASX**                 |
| Elementi figlio  | **voce**, **ENTRYREF** |



 

## <a name="remarks"></a>Commenti

Questo elemento definisce un comportamento o un'azione eseguita da Windows Media Player quando riceve un comando script etichettato come un evento. Un evento è un particolare tipo di comando script incorporato in un flusso inviato a Windows Media Player costituito da una stringa doppia. La prima stringa è la parola "Event" e la seconda stringa è il nome dell'evento. Il nome dell'evento nella seconda stringa deve corrispondere al nome dell'evento definito nel metafile. La corrispondenza non fa distinzione tra maiuscole e minuscole. Gli eventi possono essere inviati a Windows Media Player la ricezione di un flusso in tempo reale oppure possono essere salvati in un file. ASF,. WMA o. WMV che viene recapitato come flusso unicast su richiesta. Quando Windows Media Player riceve il comando script, elabora l'evento come definito dall'elemento **Event** .

Questo elemento definisce un ambito di elementi **entry** o **ENTRYREF** elaborati ogni volta che Windows Media Player riceve il comando script con l'evento denominato. **ENTRYREF** può essere un URL che punta a una pagina ASP. Con questo elemento, è possibile specificare un comportamento per il cambio di flusso quasi in tempo reale, anziché le modifiche di flusso PreCreate usando riferimenti ad altre parti di contenuto o metafile di Windows Media.

Quando si usano le pagine ASP per generare playlist, è necessario specificare un valore per la *risposta*. Proprietà **ContentType** e la *risposta*. **scade** la proprietà nella pagina ASP a causa di problemi di latenza con Windows Media Player. *Risposta*. **ContentType** deve essere un'estensione di nome di file valida per i file di Windows Media. I tipi validi includono. ASF,. asx,. WMA,. Wax,. WMV e. wvx.

Per informazioni dettagliate sull'uso dell'oggetto **Response** in ASP, vedere Platform SDK.

Questo elemento può essere visualizzato in qualsiasi punto all'interno dell'elemento **ASX** . Se più elementi **evento** all'interno di un elemento **ASX** hanno valori identici per gli attributi del **nome** , Windows Media Player utilizza la prima occorrenza all'interno dell'elemento **ASX** e ignora tutti gli altri. Quando gli elementi dell' **evento** hanno attributi di **nome** distinti, il relativo ordine nell'elemento **ASX** non è rilevante.

Windows Media Player elimina gli eventi ricevuti durante l'elaborazione di un altro evento. L'annidamento degli eventi non è supportato. Quando Windows Media Player è in modalità di anteprima, il contenuto dell'evento non è vincolato dall'elemento **PREVIEWDURATION** . la lunghezza totale del contenuto di un evento può essere riprodotto anche se la durata dell'anteprima dell'elemento **voce** attivo scade prima della fine dell'evento.

## <a name="examples"></a>Esempio

In questo esempio, quando Windows Media Player riceve l'evento del comando per script e la stringa di comando "AdLINK" nel supporto di streaming di cui viene eseguito il rendering, Cerca nella playlist un **eventoname** "AdLINK". Windows Media Player passa dal flusso di cui viene eseguito il rendering e riproduce il contenuto a cui si fa riferimento nell' **evento**" https://example.microsoft.com/adlink.htm ".

L'attributo **entry** **CLIENTSKIP** è impostato su No per impedire che il clip dell' **evento** venga ignorato. Deve essere riprodotto.

Lo script `WHENDONE="RESUME"` indica a Windows Media Player di riprendere la riproduzione del supporto precedente passato da non appena AdLINK. ASF è terminato.


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Modello a oggetti di Windows Media Player**](windows-media-player-object-model.md)
</dt> </dl>

 

 





