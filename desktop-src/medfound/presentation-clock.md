---
description: Orologio di presentazione
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Orologio di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61ad02537a2591c681db78721376651f7854ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130490"
---
# <a name="presentation-clock"></a>Orologio di presentazione

Il *clock di presentazione* è un oggetto che genera il tempo di clock per una presentazione. Il tempo segnalato dal clock di presentazione è denominato *tempo di presentazione*. Tutti i flussi in una presentazione vengono sincronizzati con l'ora di presentazione. Il clock di presentazione espone le interfacce seguenti.



| Interfaccia                                            | Descrizione                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interfaccia principale per l'uso del clock di presentazione. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Controlla la frequenza di clock.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Fornisce un callback del timer.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Arresta il clock di presentazione.                  |



 

I sink di supporto usano l'ora di presentazione per pianificare quando eseguire il rendering degli esempi. Ogni volta che un sink multimediale riceve un nuovo esempio, ottiene il timestamp dall'esempio ed esegue il rendering dell'esempio all'ora indicata o il più vicino possibile. Poiché tutti i sink di supporto in una topologia condividono lo stesso clock di presentazione, vengono sincronizzati più flussi (ad esempio audio e video). Le origini e le trasformazioni dei supporti non utilizzano il clock di presentazione, perché non pianificano il momento in cui recapitare gli esempi. Producono invece campioni ogni volta che la pipeline richiede un nuovo campione.

Se si usa la sessione multimediale per la riproduzione, la sessione multimediale gestisce tutti i dettagli relativi alla creazione del clock di presentazione, alla selezione di un'origine dell'ora e alla notifica dei sink dei supporti. L'applicazione potrebbe utilizzare il clock di presentazione per ottenere l'ora di presentazione corrente durante la riproduzione, ma in caso contrario non chiamerà alcun metodo sul clock di presentazione.

## <a name="clock-time-and-clock-states"></a>Stati di clock e clock

Per ottenere l'ora dell'orologio più recente dal clock di presentazione, chiamare [**IMFPresentationClock:: GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). I tempi di clock sono sempre in unità di 100 nanosecondi, quindi un secondo è 10 milioni (10 ^ 7) Tick. Corrisponde a una frequenza di 10 MHz.

Il clock di presentazione ha tre stati: in esecuzione, sospesa e arrestata.

-   Per eseguire l'orologio, chiamare [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). Il metodo **Start** specifica l'ora di inizio del clock. Mentre il clock è in esecuzione, il tempo di clock viene incrementato dall'ora di inizio, alla frequenza di clock corrente.
-   Per sospendere l'orologio, chiamare [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Mentre il clock viene sospeso, il tempo di clock non avanza e [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) restituisce l'ora in cui il clock è stato sospeso.
-   Per arrestare l'orologio, chiamare [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Quando il clock viene arrestato, il tempo di clock non avanza e [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) restituisce zero.

Per impostazione predefinita, l'orologio avanza a una velocità di 1,0, ovvero 1 tick per 100 nanosecondi. Per modificare la frequenza con cui avanza il clock, eseguire una query sul clock di presentazione per l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e chiamare [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

Gli oggetti possono ricevere notifiche delle modifiche di stato (incluse le modifiche di frequenza) dal clock di presentazione. Per ricevere le notifiche, implementare l'interfaccia [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e chiamare [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) sul clock di presentazione. Prima di arrestare, chiamare [**IMFPresentationClock:: RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) per annullare la registrazione dell'oggetto. I sink di supporto usano questo meccanismo per ricevere notifiche dal clock.

## <a name="presentation-times"></a>Tempi di presentazione

Un sink multimediale tenta di pianificare ogni esempio in modo che l'esempio venga sottoposto a rendering all'ora corretta o quanto più vicino possibile al tempo corretto. Si applicano le seguenti definizioni:

-   *Tempo di presentazione.* Data e ora in cui deve essere eseguito il rendering di un campione. Il tempo è espresso in unità di 100 nanosecondi.
-   *Tempo dei supporti.* Tempo relativo all'inizio del contenuto. Se, ad esempio, un file video ha una lunghezza di 10 secondi, il tempo medio per il file è pari a 5 secondi.
-   *Timestamp.* Ora contrassegnata in un esempio multimediale. Per ottenere il timestamp, chiamare [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Quando un'origine multimediale produce un esempio, imposta il timestamp uguale al tempo dei supporti. La sessione multimediale converte il timestamp nel tempo di presentazione.

Per impostazione predefinita, il tempo dei supporti e l'ora di presentazione sono gli stessi, ad esempio se un frame video viene visualizzato in 5 secondi nel file di origine, il tempo dei supporti e l'ora di presentazione sono entrambi 5 secondi. Se si utilizza l' [origine sequencer](sequencer-source.md), il modello di temporizzazione è leggermente più complesso, per consentire transizioni uniformi tra i segmenti. Per altre informazioni sul modello di temporizzazione dell'origine di Sequencer, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).

L'origine multimediale imposta sempre il timestamp uguale al tempo dei supporti. Se l'ora di presentazione non è allineata con il tempo del supporto, la sessione multimediale converte i timestamp sugli esempi di supporti. Nel momento in cui il sink riceve un campione, il timestamp dell'esempio è stato convertito in tempo di presentazione. Il sink pianifica l'esempio rispetto all'ora corrente del clock di presentazione. I sink senza frequenza sono un'eccezione, perché ignorano il clock di presentazione.

Se l'applicazione cerca una nuova posizione, la sessione multimediale riavvia il clock di presentazione in corrispondenza del tempo di ricerca specificato. Se, ad esempio, l'applicazione cerca la posizione di 5 secondi nel file, la sessione multimediale avvia l'orologio a 5 secondi. L'origine multimediale potrebbe recapitare campioni con un timestamp leggermente precedente se il tempo di ricerca non rientra in un limite del fotogramma chiave. Questa operazione è necessaria in modo che i decodificatori possano decodificare tutti i frame. La sessione multimediale Elimina o taglia gli esempi prima che raggiungano i sink multimediali, in modo da corrispondere al tempo di ricerca richiesto. Se, ad esempio, il tempo di ricerca è di 5 secondi, il primo campione audio potrebbe iniziare a 4,5 secondi. La sessione multimediale eliminerà i primi 0,5 secondi dal primo campione audio decodificato.

## <a name="creating-the-presentation-clock"></a>Creazione del clock di presentazione

Per creare il clock di presentazione, chiamare [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Per arrestare l'orologio, eseguire una query per l'interfaccia [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) e chiamare [**IMFShutdown:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). Il chiamante di **MFCreatePresentationClock** è responsabile della chiamata di **Shutdown**; nella maggior parte dei casi, si tratta della sessione multimediale anziché dell'applicazione.

## <a name="presentation-time-sources"></a>Origini ora presentazione

Nonostante il nome, il clock di presentazione non implementa effettivamente un clock. Ottiene invece i tempi di clock da un altro oggetto, denominato *origine dell'ora di presentazione*. L'origine dell'ora può essere qualsiasi oggetto che genera tick di clock accurati ed espone l'interfaccia [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Questo processo viene illustrato nella figura seguente.

![diagramma che mostra la relazione tra il clock di presentazione e l'origine dell'ora di presentazione](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Quando il clock di presentazione viene creato per la prima volta, non dispone di un'origine dell'ora. Per impostare l'origine dell'ora, chiamare [**IMFPresentationClock:: SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) con un puntatore all'interfaccia [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) dell'origine dell'ora. Un'origine ora supporta gli stessi Stati del clock di presentazione (in esecuzione, sospesa e arrestata) e deve implementare l'interfaccia [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) . Il clock di presentazione usa questa interfaccia per notificare all'origine dell'ora quando modificare lo stato. In questo modo, l'origine dell'ora fornisce i tick dell'orologio, ma il clock di presentazione avvia le modifiche di stato nell'orologio.

Alcuni sink di supporto hanno accesso a un clock accurato e pertanto espongono l'interfaccia [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . In particolare, il renderer audio può utilizzare la frequenza della scheda audio come clock. Nella riproduzione audio, il renderer audio può fungere da origine dell'ora, in modo che il video venga sincronizzato con la frequenza di riproduzione audio. Questo genere produce risultati migliori rispetto al tentativo di abbinare l'audio a un orologio esterno.

Media Foundation fornisce anche un'origine dell'ora di presentazione basata sul clock di sistema. Per creare questo oggetto, chiamare [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). L'origine dell'ora di sistema può essere usata quando nessun sink multimediale fornisce un'origine dell'ora.

In generale, un sink multimediale deve utilizzare il clock di presentazione fornito, indipendentemente dall'origine dell'ora utilizzata dal clock di presentazione. Questa regola si applica anche quando un sink multimediale implementa [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource). Se il clock di presentazione usa un'altra origine ora, il sink multimediale deve seguire tale origine dell'ora, non il proprio clock interno.

Ci sono due situazioni in cui un sink multimediale non seguirà il clock di presentazione:

-   Alcuni sink di supporto sono *senza frequenza*. Se un sink multimediale è senza frequenza, utilizza gli esempi il più rapidamente possibile, senza pianificarli in base al clock di presentazione. In genere, i sink senza frequenza scrivono i dati in un file, pertanto è consigliabile completare l'operazione il più rapidamente possibile. Un sink senza frequenza restituisce il \_ flag MEDIASINK senza frequenza nel metodo [**IMFMediaSink:: getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Quando tutti i sink in una topologia sono senza frequenza, la sessione multimediale esegue il push dei dati attraverso la pipeline il più rapidamente possibile.

-   Alcuni sink di supporto non possono corrispondere alle frequenze con un'origine ora diversa da se stessi. In tal caso, il sink restituisce il MEDIASINK \_ non può \_ corrispondere al \_ flag di clock nel metodo [**getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . La pipeline può comunque utilizzare un'altra origine ora, ma i risultati saranno inferiori a quelli ottimali. È probabile che il sink si trovi dietro e causi problemi durante la riproduzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



