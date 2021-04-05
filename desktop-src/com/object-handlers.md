---
title: Gestori di oggetti
description: Gestori di oggetti
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855645"
---
# <a name="object-handlers"></a>Gestori di oggetti

Se un'applicazione server OLE è un server locale, vale a dire che viene eseguita nel proprio spazio di elaborazione, la comunicazione tra il contenitore e il server deve essere eseguita tra i limiti del processo. Poiché questo processo è dispendioso, OLE si basa su un oggetto surrogato caricato nello spazio di processo del contenitore per agire per conto di un'applicazione server locale. Questo oggetto surrogato, noto come *gestore di oggetti*, richiede il contenitore dei servizi che non richiedono l'attenzione dell'applicazione server, ad esempio le richieste di disegno. Quando un contenitore richiede un elemento che non può essere fornito dal gestore di oggetti, il gestore comunica con l'applicazione server utilizzando il meccanismo di comunicazione out-of-process di COM.

Un gestore di oggetti è univoco per una classe di oggetti. Quando si crea un'istanza di un gestore per una classe, non è possibile utilizzarla per un'altra classe. Quando viene usato per un documento composto, il gestore dell'oggetto implementa le strutture dei dati sul lato contenitore quando si accede in remoto agli oggetti di una determinata classe.

OLE fornisce un gestore di oggetti predefinito che può essere utilizzato dalle applicazioni server locali. Per le applicazioni che richiedono comportamenti speciali, gli sviluppatori possono implementare un gestore personalizzato che sostituisce il gestore predefinito o lo usa per fornire determinati comportamenti predefiniti.

Un gestore di oggetti è una DLL che contiene diversi componenti di interazione. Questi componenti includono parti remote per gestire la comunicazione tra il gestore e la relativa applicazione server, una cache per archiviare i dati di un oggetto, oltre a informazioni sulla modalità di formattazione e visualizzazione dei dati e un oggetto di controllo che coordina le attività degli altri componenti della DLL. Inoltre, se un oggetto è un collegamento, la DLL include anche un componente di collegamento, o un *oggetto collegato*, che tiene traccia del nome e della posizione dell'origine del collegamento.

La *cache* contiene dati e informazioni di presentazione sufficienti affinché il gestore visualizzi un oggetto caricato, ma non in esecuzione, nel relativo contenitore. OLE fornisce un'implementazione della cache utilizzata dal gestore dell'oggetto predefinito OLE e dall'oggetto collegamento. La cache archivia i dati in formati necessari al gestore dell'oggetto per soddisfare le richieste di estrazione del contenitore. Quando si modificano i dati di un oggetto, l'oggetto invia una notifica alla cache in modo da consentire l'esecuzione di un aggiornamento. Per ulteriori informazioni sulla cache, vedere [View Caching](view-caching.md).

Per altre informazioni, vedere l'argomento seguente:

-   [Gestore predefinito e gestori personalizzati](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




