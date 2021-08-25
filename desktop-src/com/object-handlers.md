---
title: Gestori di oggetti
description: Gestori di oggetti
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85221456d637e0d9e982aad253c06d34618018a3648a31a7bd21e8c1465fa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992321"
---
# <a name="object-handlers"></a>Gestori di oggetti

Se un'applicazione server OLE è un server locale, ovvero viene eseguita nel proprio spazio di elaborazione, la comunicazione tra contenitore e server deve avvenire attraverso i limiti del processo. Poiché questo processo è costoso, OLE si basa su un oggetto surrogato caricato nello spazio di elaborazione del contenitore per agire per conto di un'applicazione server locale. Questo oggetto surrogato, noto come gestore di oggetti *,* gestisce le richieste del contenitore che non richiedono l'attenzione dell'applicazione server, ad esempio le richieste di disegno. Quando un contenitore richiede qualcosa che il gestore oggetti non può fornire, comunica con l'applicazione server usando il meccanismo di comunicazione out-of-process di COM.

Un gestore di oggetti è univoco per una classe di oggetti. Quando si crea un'istanza di un gestore per una classe, non è possibile usarla per un'altra. Quando viene usato per un documento composto, il gestore di oggetti implementa le strutture dei dati sul lato contenitore quando si accede in modalità remota agli oggetti di una determinata classe.

OLE fornisce un gestore di oggetti predefinito che le applicazioni server locali possono usare. Per le applicazioni che richiedono comportamenti speciali, gli sviluppatori possono implementare un gestore personalizzato che sostituisce il gestore predefinito o lo usa per fornire determinati comportamenti predefiniti.

Un gestore di oggetti è una DLL contenente diversi componenti che interagiscono. Questi componenti includono parti di comunicazione remota per gestire la comunicazione tra il gestore e la relativa applicazione server, una cache per l'archiviazione dei dati di un oggetto, oltre a informazioni su come tali dati devono essere formattati e visualizzati e un oggetto di controllo che coordina le attività degli altri componenti della DLL. Inoltre, se un oggetto è un collegamento, la DLL include anche un componente di collegamento o un oggetto collegato *,* che tiene traccia del nome e del percorso dell'origine del collegamento.

La *cache* contiene dati e informazioni di presentazione sufficienti per il gestore per visualizzare un oggetto caricato, ma non in esecuzione, nel relativo contenitore. OLE fornisce un'implementazione della cache utilizzata dal gestore oggetti predefinito di OLE e dall'oggetto collegamento. La cache archivia i dati nei formati necessari al gestore di oggetti per soddisfare le richieste di disegno del contenitore. Quando i dati di un oggetto cambiano, l'oggetto invia una notifica alla cache in modo che possa verificarsi un aggiornamento. Per altre informazioni sulla cache, vedere [Visualizzare Caching](view-caching.md).

Per altre informazioni, vedere l'argomento seguente:

-   [Gestore predefinito e gestori personalizzati](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




