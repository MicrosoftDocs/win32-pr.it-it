---
title: Gestore OLE
description: Un gestore OLE è una DLL contenente diversi componenti di interazione usati per il collegamento e l'incorporamento.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecca46971d3ad4fdea7df6a502b2897439e03817849ad776d3e0b13a213a94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129633"
---
# <a name="the-ole-handler"></a>Gestore OLE

Un *gestore OLE* è una DLL contenente diversi componenti di interazione utilizzati per il collegamento e l'incorporamento. Per evitare il costo della comunicazione interprocesso costante tra un contenitore e il relativo server, il gestore viene caricato nello spazio di elaborazione del contenitore per agire per conto di un server come una sorta di processo surrogato. Il gestore OLE gestisce le richieste del contenitore che non richiedono l'attenzione dell'applicazione server, ad esempio le richieste di disegno. Quando un contenitore richiede qualcosa che il gestore di oggetti non è in grado di fornire, comunica con l'applicazione server usando il meccanismo di comunicazione out-of-process COM.

I componenti del gestore OLE includono parti remote per gestire la comunicazione tra il gestore e il relativo server, una cache per l'archiviazione dei dati di un oggetto (insieme a informazioni su come devono essere formattati e visualizzati i dati) e un oggetto di controllo che coordina le attività degli altri componenti della DLL. Inoltre, se un oggetto è un collegamento, la DLL include anche un componente di collegamento o un oggetto collegato *,* che tiene traccia del nome e del percorso dell'origine del collegamento.

OLE fornisce un gestore predefinito utilizzato dalla maggior parte delle applicazioni per il collegamento e l'incorporamento. Se il valore predefinito non corrisponde ai requisiti del server, è possibile sostituire completamente il gestore predefinito o usare parti della funzionalità che fornisce dove appropriato. Nel secondo caso, il gestore dell'applicazione viene implementato come oggetto aggregato composto da un nuovo oggetto controllo e dal gestore predefinito. I gestori applicazioni/predefiniti combinazioni sono noti anche come *gestori in-process.* Il *gestore remoto viene* usato per gli oggetti a cui non è assegnato un CLSID nel Registro di sistema o che non dispongono di un gestore specificato. Tutto ciò che è necessario da un gestore per questi tipi di oggetti è che passano informazioni attraverso il limite del processo. Per creare una nuova istanza del gestore predefinito, chiamare [**OleCreateDefaultHandler.**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler) Per alcune circostanze speciali, chiamare [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Quando si crea un'istanza di un gestore per una classe, non è possibile usarla per un'altra. Quando viene usato per un documento composto, il gestore OLE implementa le strutture di dati sul lato contenitore quando si accede in remoto agli oggetti di una determinata classe.

OLE ha definito il gestore predefinito per i client di server locali di documenti composti. Il gestore predefinito ha implementato una serie di interfacce che non sono state implementate dal server tipico. Quando SUCCESSIVAMENTE OLE consentiva i server in-process per i documenti composti, doveva creare un helper di incorporamento che implementava queste interfacce aggiuntive in modo che i client fossero in grado di integrarle facilmente.

I progettisti di framework che definiscono e implementano un gestore lato client devono considerare questo problema nella progettazione e devono fornire un helper in-process equivalente per gli stessi motivi. Anche se le finestre di progettazione attualmente non implementano interfacce nel gestore che i server non espongono, è possibile definire ora un helper in modo che possano aggiungerle in futuro. In alternativa, è possibile implementare le interfacce aggiuntive sull'oggetto server stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore Client-Side lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




