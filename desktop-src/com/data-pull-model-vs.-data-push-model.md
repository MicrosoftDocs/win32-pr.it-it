---
title: Data-Pull modello e Data-Push modello
description: Data-Pull modello e Data-Push modello
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab89f61301f9116a7e826f1965bd54f75004a3a90af8c9d1a1bc13acb1fc9c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048449"
---
# <a name="data-pull-model-and-data-push-model"></a>Data-Pull modello e Data-Push modello

Un client di un moniker asincrono può scegliere tra un modello di pull di dati e un modello di push di dati per la gestione di un'operazione [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrona e la ricezione di notifiche asincrone. Nel modello di pull dei dati, il client guida l'operazione di associazione e il moniker fornisce i dati al client solo durante la lettura. In altre parole, dopo la prima chiamata a [**IBindStatusCallback::OnDataAvailable,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))il moniker non fornisce dati al client a meno che il client non abbia utilizzato tutti i dati già disponibili.

Poiché i dati vengono scaricati solo quando vengono richiesti, i client che scelgono il modello di pull dei dati devono assicurarsi di leggere i dati in modo corretto. Nel caso di download Internet con moniker [URL](url-monikers.md), l'operazione di associazione potrebbe non riuscire se un client attende troppo tempo prima di richiedere altri dati.

Nel modello di push di dati, il moniker determina l'operazione di associazione asincrona e invia continuamente una notifica al client ogni volta che sono disponibili nuovi dati. Il client può scegliere se leggere i dati in qualsiasi momento durante l'operazione di associazione, ma il moniker determina il completamento dell'operazione di associazione indipendentemente dal fatto che venga completata.

È inoltre necessario ricordare di seguire le regole COM per l'allocazione di memoria quando si usano moniker asincroni, in particolare quanto segue:

-   Ogni volta che un'interfaccia COM o una chiamata di funzione restituisce un buffer (stringa o altro) al client, il client è responsabile del liberare la memoria chiamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
-   Ogni volta che un'interfaccia o una funzione COM richiede un buffer dal client, il client deve allocare tale buffer usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) e il chiamato deve liberarlo.

Assicurarsi di seguire queste regole durante l'allocazione di stringhe o buffer passati ai moniker asincroni e ricordare di liberare la memoria restituita dai moniker asincroni. Per [informazioni dettagliate, vedere](the-com-library.md) Gestione dell'allocazione di memoria e degli argomenti correlati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 