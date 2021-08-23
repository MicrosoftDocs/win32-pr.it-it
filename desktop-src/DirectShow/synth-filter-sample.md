---
description: Esempio di filtro synth
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Esempio di filtro synth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a3a366a6612aadf653b5af13099dbc8a4f08c2fb828bca6e64514cb1801e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291192"
---
# <a name="synth-filter-sample"></a>Esempio di filtro synth

## <a name="description"></a>Descrizione

Il filtro Synth è un filtro di origine che genera forme d'onda audio.

Questo filtro illustra la creazione dinamica di grafi. Può passare dal formato audio PCM non compresso al formato MS \_ ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) compresso.

Questo filtro viene visualizzato in GraphEdit come "Filtro sintetizzatore audio".

Per altre informazioni sulla creazione dinamica di grafi, vedere [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="usage"></a>Utilizzo

Il filtro Synth consente all'utente di impostare la forma d'onda, la frequenza, il numero di canali e altre proprietà tramite la pagina delle proprietà. Per impostare l'endpoint superiore o inferiore dell'intervallo di frequenza di scorrimento, tenere premuto MAIUSC durante la regolazione del dispositivo di scorrimento della frequenza. Il filtro supporta anche un'interfaccia personalizzata, ISynth2, per l'impostazione di queste proprietà.

Per illustrare la funzionalità di creazione dinamica dei grafi, eseguire le operazioni seguenti:

1.  Compilare il filtro e registrarlo con l'utilità Regsvr32.
2.  Avviare GraphEdit.
3.  Inserire il filtro Sintetizzatore audio. Viene visualizzato nella categoria DirectShow filtri.
4.  Eseguire il rendering del pin di output del filtro.
5.  Fare clic **sul pulsante** Riproduci.
6.  Aprire la pagina delle proprietà del filtro.
7.  Nell'area Formato di output selezionare PCM o Microsoft ADPCM.

## <a name="programming-notes"></a>Note sulla programmazione

Questo esempio contiene i file seguenti:

-   Dynsrc.h, Dynsrc.cpp: contiene due classi di base per i filtri di origine che supportano la compilazione dinamica dei grafi, CDynamicSource e CDynamicSourceStream.
-   ISynth.h: dichiara l'interfaccia ISynth2 personalizzata per l'impostazione delle proprietà nel filtro.
-   Resource.h: contiene costanti di risorsa.
-   Synth.def: esporta le funzioni DLL necessarie per la libreria COM.
-   Synth.h, Synth.cpp: contiene la classe CAudioSynth, che genera i dati audio, e la classe CSynthFilter, che implementa il filtro.
-   Synth.rc: contiene le risorse usate dal filtro.
-   Synthprp.h, Synthprp.cpp: implementa la pagina delle proprietà del filtro.

La classe CDynamicSource viene adattata dalla classe di base [**CSource.**](csource.md) Usa uno o più pin di output derivati dalla classe CDynamicSourceStream. La classe CDynamicSourceStream viene adattata dalla classe [**CSourceStream,**](csourcestream.md) ma deriva dalla classe [**CDynamicOutputPin**](cdynamicoutputpin.md) anziché dalla [**classe CBaseOutputPin.**](cbaseoutputpin.md)

La classe CDynamicSource ha i metodi seguenti non trovati in [**CSource**](csource.md):

-   Stop: segnala l'evento di arresto ([**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) e arresta il thread di lavoro per tutti i pin non collegati. Su un pin connesso, il metodo Inactive del pin arresterà il thread di lavoro.
-   Sospendi: reimposta l'evento di arresto.
-   JoinFilterGraph: chiama il [**metodo CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) su ogni pin.

La classe CDynamicSourceStream ha i metodi seguenti non trovati in [**CSourceStream**](csourcestream.md):

-   DestroySourceThread: arresta il thread di lavoro.
-   FatalError: segnala un errore al gestore del grafico dei filtri.
-   OutputPinNeedsToBeReconnected: segnala che il pin di output deve essere riconnesso. Quando viene chiamato questo metodo, il thread di lavoro chiama il metodo [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) per riconnettere il pin.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK \] Root* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Synth.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



