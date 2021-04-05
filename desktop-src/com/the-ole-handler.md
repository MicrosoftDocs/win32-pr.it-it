---
title: Gestore OLE
description: Un gestore OLE è una DLL che contiene diversi componenti di interazione usati per il collegamento e l'incorporamento.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044785"
---
# <a name="the-ole-handler"></a>Gestore OLE

Un *gestore OLE* è una dll che contiene diversi componenti di interazione usati per il collegamento e l'incorporamento. Per evitare il costo della comunicazione costante interprocesso tra un contenitore e il relativo server, il gestore viene caricato nello spazio di processo del contenitore per agire per conto di un server come un tipo di processo surrogato. Il gestore OLE gestisce le richieste del contenitore che non richiedono l'attenzione dell'applicazione server, ad esempio le richieste di disegno. Quando un contenitore richiede un elemento che non può essere fornito dal gestore di oggetti, il gestore comunica con l'applicazione server utilizzando il meccanismo di comunicazione out-of-process COM.

I componenti del gestore OLE includono parti remote per gestire la comunicazione tra il gestore e il relativo server, una cache per archiviare i dati di un oggetto (insieme alle informazioni sul modo in cui i dati devono essere formattati e visualizzati) e un oggetto di controllo che coordina le attività degli altri componenti della DLL. Inoltre, se un oggetto è un collegamento, la DLL include anche un componente di collegamento, o un *oggetto collegato*, che tiene traccia del nome e della posizione dell'origine del collegamento.

OLE fornisce un gestore predefinito usato dalla maggior parte delle applicazioni per il collegamento e l'incorporamento. Se il valore predefinito non corrisponde ai requisiti del server, è possibile sostituire completamente il gestore predefinito o usare parti della funzionalità che fornisce laddove appropriato. Nel secondo caso, il gestore dell'applicazione viene implementato come un oggetto aggregato costituito da un nuovo oggetto controllo e dal gestore predefinito. I gestori di applicazione/predefiniti combinati sono noti anche come *gestori in-process*. Il *gestore di comunicazione remota* viene usato per gli oggetti a cui non è assegnato un CLSID nel registro di sistema o che non hanno alcun gestore specificato. Tutto ciò che è necessario da un gestore per questi tipi di oggetti è che passano informazioni attraverso il limite del processo. Per creare una nuova istanza del gestore predefinito, chiamare [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). Per alcune circostanze particolari, chiamare [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Quando si crea un'istanza di un gestore per una classe, non è possibile utilizzarla per un'altra classe. Se utilizzata per un documento composto, il gestore OLE implementa le strutture dei dati sul lato contenitore quando si accede in remoto agli oggetti di una determinata classe.

OLE definisce il gestore predefinito per i client dei server locali del documento composito. Il gestore predefinito ha implementato una serie di interfacce che non sono state eseguite dal server tipico. Quando OLE consentiva successivamente ai server in-process i documenti composti, era necessario creare un helper di incorporamento che implementasse queste interfacce aggiuntive in modo che i client potessero lavorare senza interruzioni.

I progettisti di Framework che definiscono e implementano un gestore sul lato client devono considerare questo problema nella progettazione e devono fornire un helper in-process equivalente per gli stessi motivi. Anche se le finestre di progettazione non implementano attualmente le interfacce nel gestore che i server non espongono, potrebbe voler definire un helper per poterle aggiungere in futuro. In alternativa, è possibile implementare le interfacce aggiuntive sull'oggetto server stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore di Client-Side Lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




