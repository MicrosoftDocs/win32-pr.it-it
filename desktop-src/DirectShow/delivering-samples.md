---
description: Distribuzione di esempi
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Distribuzione di esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401347"
---
# <a name="delivering-samples"></a>Distribuzione di esempi

Questo articolo descrive come un filtro fornisce un esempio. Descrive il modello push, usando i metodi [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e il modello pull, usando [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Modello push: distribuzione di un esempio**

Il pin di output recapita un esempio chiamando il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) , che è equivalente ma fornisce una matrice di esempi. Il pin di input può bloccarsi all'interno di **Receive** (o **ReceiveMultiple**). Se il PIN potrebbe bloccarsi, il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) deve restituire S \_ OK. Se il PIN non garantisce mai il blocco, **ReceiveCanBlock** deve restituire S \_ false. Il \_ valore restituito S OK non significa che **Receive** always Blocks, solo che potrebbe.

Sebbene la **ricezione** possa essere bloccata in modo da attendere la disponibilità di una risorsa, non dovrebbe bloccarsi in attesa di più dati dal filtro upstream. Questa operazione può causare un deadlock in cui il filtro upstream attende il rilascio dell'esempio da parte del filtro downstream, che non si verifica mai perché il filtro downstream è in attesa sul filtro upstream. Se un filtro ha più pin di input, tuttavia, un pin può attendere la ricezione dei dati da parte di un altro pin. Ad esempio, il filtro [Mux AVI](avi-mux-filter.md) esegue questa operazione in modo che possa interleave dati audio e video.

Un PIN potrebbe rifiutare un campione per diversi motivi:

-   Il PIN sta per essere scaricato (vedere [scaricamento](flushing.md)).
-   Il PIN non è connesso.
-   Il filtro è stato arrestato.
-   Si è verificato un altro errore.

Il metodo **Receive** deve restituire S \_ false nel primo caso e un codice di errore negli altri casi. Il filtro upstream deve interrompere l'invio di esempi quando il codice restituito è diverso da S \_ OK.

È possibile considerare i primi tre casi come errori "previsti", nel senso che lo stato del filtro era errato per la ricezione degli esempi. Un errore imprevisto potrebbe essere uno che fa sì che il pin rifiuti un campione anche se il pin si trova in uno stato di ricezione. Se si verifica un errore di questo tipo, il PIN deve inviare una notifica di fine flusso a valle e inviare un evento [**\_ ERRORABORT EC**](ec-errorabort.md) a Filter Graph Manager.

Nelle classi di base di DirectShow, il metodo [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) controlla i casi di errore generali: svuotamento, arrestato e così via. La classe derivata deve verificare la presenza di errori specifici del filtro. In caso di errore, il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) Invia la notifica di fine flusso e l' \_ evento ERRORABORT EC.

**Modello pull: richiesta di un esempio**

Nell'interfaccia **IAsyncReader** il pin di input richiede esempi dal pin di output chiamando uno dei metodi seguenti:

-   [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

Il metodo di **richiesta** è asincrono. il pin di input chiama [**IAsyncReader:: WaitForNext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) per attendere il completamento della richiesta. Gli altri due metodi sono sincroni.

**Quando recapitare i dati**

Un filtro recapita sempre gli esempi mentre è nello stato in esecuzione. Nella maggior parte dei casi, un filtro fornisce anche esempi mentre è in pausa. Ciò consente al grafico di individuare i dati in modo che la riproduzione venga avviata immediatamente quando viene chiamata l' **esecuzione** (vedere [Stati di filtro](filter-states.md)). Se il filtro non recapita i dati mentre è in pausa, il metodo **IMediaFilter:: GetState** del filtro deve restituire \_ \_ il segnale del cant di VFW \_ nello stato sospeso. Questo codice restituito segnala al grafico del filtro di non attendere i dati dal filtro prima di completare la transizione di sospensione. In caso contrario, il metodo **pause** si bloccherà a tempo indefinito. Per un esempio di codice, vedere [**CBaseFilter:: GetState**](cbasefilter-getstate.md).

Di seguito sono riportati alcuni esempi di quando un filtro potrebbe dover restituire il CUE del cant di VFW \_ \_ \_ :

-   Le origini live, ad esempio i filtri di acquisizione, non devono inviare dati mentre sono sospesi. Vedere [produzione di dati in un filtro di acquisizione](producing-data-in-a-capture-filter.md).
-   Un filtro Splitter può inviare o meno dati in pausa, a seconda dell'implementazione. Se il filtro usa thread distinti per accodare i dati in ogni pin di output, può inviare i dati mentre sono sospesi. Tuttavia, se il filtro usa un solo thread per ogni pin di output, il primo PIN potrebbe bloccare il thread quando chiama **Receive**, in modo da impedire agli altri pin di inviare dati. In tal caso, è necessario restituire il \_ cue di VFW S \_ cant \_ .
-   Un filtro può recapitare i dati sporadicamente. Ad esempio, potrebbe analizzare un flusso di dati personalizzato e filtrare alcuni pacchetti e distribuirne altri. In tal caso, è possibile che al filtro non venga garantito il recapito dei dati mentre sono sospesi.

Un filtro di origine (usando il modello push) o un filtro del parser (usando il modello push/pull) crea uno o più thread di streaming, che forniscono i campioni il più rapidamente possibile. I filtri downstream, ad esempio i decodificatori e le trasformazioni, in genere inviano i dati solo quando viene chiamato **Receive** sui rispettivi pin di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricezione e distribuzione di esempi](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



