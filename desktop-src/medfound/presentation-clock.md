---
description: Orologio presentazione
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Orologio presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0219b6384373fd75bc8a424935e502841071f69eaa9ae719ec6ed35c950218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239161"
---
# <a name="presentation-clock"></a>Orologio presentazione

*L'orologio della* presentazione è un oggetto che genera l'ora dell'orologio per una presentazione. L'ora segnalata dall'orologio della presentazione è denominata *ora di presentazione.* Tutti i flussi di una presentazione vengono sincronizzati con l'ora di presentazione. L'orologio di presentazione espone le interfacce seguenti.



| Interfaccia                                            | Descrizione                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interfaccia primaria per l'uso dell'orologio di presentazione. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Controlla la frequenza dell'orologio.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Fornisce un callback del timer.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Arresta l'orologio della presentazione.                  |



 

I sink multimediali usano il tempo di presentazione per pianificare quando eseguire il rendering degli esempi. Ogni volta che un sink multimediale riceve un nuovo esempio, ottiene il timestamp dell'esempio ed esegue il rendering dell'esempio all'ora indicata o il più vicino possibile a tale ora. Poiché tutti i sink multimediali in una topologia condividono lo stesso clock di presentazione, vengono sincronizzati più flussi, ad esempio audio e video. Le origini multimediali e le trasformazioni non usano l'orologio della presentazione, perché non pianificano quando distribuire gli esempi. Generano invece campioni ogni volta che la pipeline richiede un nuovo esempio.

Se si usa la sessione multimediale per la riproduzione, la sessione multimediale gestisce tutti i dettagli relativi alla creazione dell'orologio della presentazione, alla selezione di un'origine ora e alla notifica dei sink multimediali. L'applicazione potrebbe usare l'orologio della presentazione per ottenere l'ora di presentazione corrente durante la riproduzione, ma in caso contrario non chiamerà alcun metodo sull'orologio della presentazione.

## <a name="clock-time-and-clock-states"></a>Stati dell'ora e dell'orologio

Per ottenere l'ora più recente dall'orologio della presentazione, chiamare [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). Gli orari di clock sono sempre in unità di 100 nanosecondi, quindi un secondo è 10.000.000 (10^7) tick. Corrisponde a una frequenza di 10 MHz.

L'orologio della presentazione ha tre stati: In esecuzione, Sospeso e Arrestato.

-   Per eseguire l'orologio, chiamare [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). Il **metodo Start** specifica l'ora di inizio dell'orologio. Mentre l'orologio è in esecuzione, l'ora dell'orologio viene incrementata dall'ora di inizio, alla frequenza di clock corrente.
-   Per sospendere l'orologio, chiamare [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Mentre l'orologio è in pausa, l'ora dell'orologio non avanza e [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) restituisce l'ora in cui l'orologio è stato sospeso.
-   Per arrestare l'orologio, chiamare [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Quando l'orologio viene arrestato, l'ora dell'orologio non avanza e [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) restituisce zero.

Per impostazione predefinita, l'orologio avanza a una velocità di 1,0, ovvero 1 tick per 100 nanosecondi. Per modificare la velocità di avanzamento dell'orologio, eseguire una query sull'orologio di presentazione per [**l'interfaccia IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e chiamare [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

Gli oggetti possono ricevere notifiche di modifiche dello stato (incluse le modifiche della frequenza) dall'orologio della presentazione. Per ricevere notifiche, implementare [**l'interfaccia IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e chiamare [**IMFPresentationClock::AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) sull'orologio della presentazione. Prima dell'arresto, chiamare [**IMFPresentationClock::RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) per annullare la registrazione dell'oggetto. I sink multimediali usano questo meccanismo per ricevere notifiche dall'orologio.

## <a name="presentation-times"></a>Orari di presentazione

Un sink multimediale tenta di pianificare ogni esempio in modo che il rendering dell'esempio sia corretto o il più vicino possibile all'ora corretta. Si applicano le definizioni seguenti:

-   *Ora di presentazione.* Ora in cui deve essere eseguito il rendering di un esempio. Il tempo è specificato in unità di 100 nanosecondi.
-   *Tempo multimediale.* Ora relativa all'inizio del contenuto. Ad esempio, se un file video è lungo 10 secondi, il punto a metà del file ha un tempo multimediale di 5 secondi.
-   *Timestamp.* Ora contrassegnata in un campione di supporti. Per ottenere il timestamp, chiamare [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Quando un'origine multimediale produce un campione, imposta il timestamp uguale all'ora del supporto. La sessione multimediale converte il timestamp in ora di presentazione.

Per impostazione predefinita, il tempo multimediale e l'ora di presentazione sono gli stessi, ad esempio, se un fotogramma video viene visualizzato 5 secondi nel file di origine, il tempo multimediale e il tempo di presentazione sono entrambi di 5 secondi. Se si usa l'origine [sequencer](sequencer-source.md), il modello di temporizzazione è un po' più complesso, per abilitare transizioni uniformi tra segmenti. Per altre informazioni sul modello di temporizzazione dell'origine sequencer, vedere [Sequenza dei tempi di presentazione.](sequence-presentation-times.md)

L'origine del supporto imposta sempre il timestamp uguale all'ora del supporto. Se l'ora di presentazione non è allineata all'ora del supporto, la sessione multimediale converte i timestamp sugli esempi di supporti. Quando il sink riceve un esempio, il timestamp dell'esempio è stato convertito in ora di presentazione. Il sink pianifica l'esempio in base all'ora corrente dell'orologio della presentazione. I sink senza frequenza sono un'eccezione perché ignorano l'orologio della presentazione.

Se l'applicazione cerca una nuova posizione, la sessione multimediale riavvia l'orologio della presentazione all'ora di ricerca specificata. Ad esempio, se l'applicazione cerca la posizione di 5 secondi nel file, la sessione multimediale avvia l'orologio a 5 secondi. L'origine multimediale potrebbe fornire campioni con un timestamp leggermente precedente se il tempo di ricerca non rientra in un limite del fotogramma chiave. Questa operazione è necessaria in modo che i decodificatori possano decodificare tutti i fotogrammi. La sessione multimediale elimina o taglia i campioni prima che raggiungano i sink multimediali, in modo che corrispondano al tempo di ricerca richiesto. Ad esempio, se il tempo di ricerca è di 5 secondi, il primo campione audio potrebbe iniziare a 4,5 secondi. La sessione multimediale taglia i primi 0,5 secondi dal primo campione audio decodificato.

## <a name="creating-the-presentation-clock"></a>Creazione dell'orologio della presentazione

Per creare l'orologio della presentazione, chiamare [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Per arrestare l'orologio, eseguire una query per [**l'interfaccia IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) e chiamare [**IMFShutdown::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). Il chiamante **di MFCreatePresentationClock** è responsabile della chiamata di **Shutdown**. nella maggior parte dei casi si tratta della sessione multimediale anziché dell'applicazione.

## <a name="presentation-time-sources"></a>Origini dell'ora di presentazione

Nonostante il nome, l'orologio di presentazione non implementa effettivamente un orologio. Ottiene invece l'ora dell'orologio da un altro oggetto, denominato origine *dell'ora di presentazione.* L'origine dell'ora può essere qualsiasi oggetto che genera tick di clock accurati ed espone [**l'interfaccia IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) Questo processo viene illustrato nella figura seguente.

![diagramma che mostra la relazione tra l'orologio della presentazione e l'origine dell'ora di presentazione](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Quando viene creato per la prima volta, l'orologio della presentazione non ha un'origine ora. Per impostare l'origine ora, chiamare [**IMFPresentationClock::SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) con un puntatore [**all'interfaccia IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) dell'origine ora. Un'origine ora supporta gli stessi stati dell'orologio della presentazione (in esecuzione, sospesa e interrotta) e deve implementare [**l'interfaccia IMFClockStateSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) L'orologio della presentazione usa questa interfaccia per notificare all'origine dell'ora quando modificare lo stato. In questo modo, l'origine ora fornisce i tick dell'orologio, ma l'orologio di presentazione avvia le modifiche di stato nell'orologio.

Alcuni sink multimediali hanno accesso a un clock accurato e pertanto espongono [**l'interfaccia IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) In particolare, il renderer audio può usare la frequenza della scheda audio come orologio. Nella riproduzione audio è utile che il renderer audio funzioni come origine ora, in modo che il video sia sincronizzato con la velocità di riproduzione audio. Questo in genere produce risultati migliori rispetto al tentativo di associare l'audio a un clock esterno.

Media Foundation fornisce anche un'origine ora di presentazione basata sull'orologio di sistema. Per creare questo oggetto, chiamare [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). L'origine ora di sistema può essere usata quando nessun sink multimediale fornisce un'origine ora.

In generale, un sink multimediale deve usare l'orologio di presentazione fornito, indipendentemente dall'origine dell'ora utilizzata dall'orologio della presentazione. Questa regola si applica anche quando un sink multimediale implementa [**IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) Se l'orologio della presentazione usa un'altra origine ora, il sink multimediale deve seguire tale origine ora, non il proprio orologio interno.

Esistono due situazioni in cui un sink multimediale non segue l'orologio della presentazione:

-   Alcuni sink multimediali sono *senza frequenza.* Se un sink multimediale è senza frequenza, usa gli esempi il più rapidamente possibile, senza pianificarli in base all'orologio della presentazione. In genere, i sink senza frequenza scrivono dati in un file, pertanto è consigliabile completare l'operazione il più rapidamente possibile. Un sink senza frequenza restituisce il flag MEDIASINK RATELESS nel metodo \_ [**IMFMediaSink::GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) Quando tutti i sink in una topologia sono senza frequenza, la sessione multimediale esegue il push dei dati attraverso la pipeline il più rapidamente possibile.

-   Alcuni sink multimediali non possono corrispondere alle frequenze con un'origine ora diversa da se stessi. In tal caso, il sink restituisce il flag MEDIASINK \_ CANNOT MATCH CLOCK nel metodo \_ \_ [**GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) La pipeline può comunque usare un'altra origine ora, ma i risultati saranno inferiori a quelli ottimali. Il sink probabilmente cadrà indietro e causerà problemi durante la riproduzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation API della piattaforma](media-foundation-platform-apis.md)
</dt> </dl>

 

 



