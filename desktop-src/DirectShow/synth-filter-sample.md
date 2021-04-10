---
description: Esempio di filtro synth
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Esempio di filtro synth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885162"
---
# <a name="synth-filter-sample"></a>Esempio di filtro synth

## <a name="description"></a>Descrizione

Il filtro synth è un filtro di origine che genera le forme d'onda audio.

Questo filtro illustra la compilazione dinamica del grafico. Può passare dal formato audio PCM non compresso a quello compresso MS \_ ADPCM (Microsoft Adaptive Delta Pulse Code Modulation).

Questo filtro viene visualizzato in GraphEdit come "filtro del sintetizzatore audio".

Per ulteriori informazioni sulla compilazione dinamica dei grafici, vedere [compilazione dinamica dei grafici](dynamic-graph-building.md).

## <a name="usage"></a>Utilizzo

Il filtro synth consente all'utente di impostare la forma d'onda, la frequenza, il numero di canali e altre proprietà tramite la pagina delle proprietà. Per impostare l'endpoint superiore o inferiore dell'intervallo di frequenza di sweep, tenere premuto MAIUSC mentre si modifica il dispositivo di scorrimento della frequenza. Il filtro supporta inoltre un'interfaccia personalizzata, ISynth2, per l'impostazione di queste proprietà.

Per dimostrare la funzionalità di compilazione dinamica dei grafici, procedere come segue:

1.  Compilare il filtro e registrarlo con l'utilità regsvr32.
2.  Avviare GraphEdit.
3.  Inserire il filtro del sintetizzatore audio. Viene visualizzato nella categoria filtri DirectShow.
4.  Eseguire il rendering del PIN di output del filtro.
5.  Fare clic sul pulsante **Riproduci** .
6.  Aprire la pagina delle proprietà del filtro.
7.  Nell'area formato di output Selezionare PCM o Microsoft ADPCM.

## <a name="programming-notes"></a>Note sulla programmazione

Questo esempio contiene i file seguenti:

-   DYNSRC. h, DYNSRC. cpp: contiene due classi di base per i filtri di origine che supportano la compilazione dinamica dei grafici, CDynamicSource e CDynamicSourceStream.
-   ISynth. h: dichiara l'interfaccia ISynth2 personalizzata per l'impostazione delle proprietà nel filtro.
-   Resource. h: contiene costanti di risorsa.
-   Synth. def: Esporta le funzioni DLL richieste dalla libreria COM.
-   Synth. h, synth. cpp: contiene la classe CAudioSynth, che genera i dati audio e la classe CSynthFilter, che implementa il filtro.
-   Synth. RC: contiene le risorse usate dal filtro.
-   Synthprp. h, Synthprp. cpp: implementa la pagina delle proprietà del filtro.

La classe CDynamicSource è adattata dalla classe di base [**CSource**](csource.md) . Usa uno o più pin di output derivati dalla classe CDynamicSourceStream. La classe CDynamicSourceStream è adattata dalla classe [**CSourceStream**](csourcestream.md) , ma deriva dalla classe [**CDynamicOutputPin**](cdynamicoutputpin.md) anziché dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) .

Per la classe CDynamicSource non sono stati trovati i metodi seguenti in [**CSource**](csource.md):

-   Stop: segnala l'evento Stop ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) e arresta il thread di lavoro per tutti i pin non connessi. Su un pin connesso, il metodo inattivo del pin arresterà il thread di lavoro.
-   Pause: Reimposta l'evento Stop.
-   JoinFilterGraph: chiama il metodo [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) per ogni pin.

Per la classe CDynamicSourceStream non sono stati trovati i metodi seguenti in [**CSourceStream**](csourcestream.md):

-   DestroySourceThread: arresta il thread di lavoro.
-   FatalError: segnala un errore al gestore del grafico dei filtri.
-   OutputPinNeedsToBeReconnected: segnala che è necessario riconnettere il pin di output. Quando viene chiamato questo metodo, il thread di lavoro chiama il metodo [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) per riconnettere il PIN.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel seguente percorso: *\[ SDK \] radice* \\ esempi di \\ \\ filtri DirectShow \\ Multimedia \\ synth.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



