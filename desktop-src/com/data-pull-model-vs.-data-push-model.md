---
title: Modello di Data-Pull e modello di Data-Push
description: Modello di Data-Pull e modello di Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399800"
---
# <a name="data-pull-model-and-data-push-model"></a>Modello di Data-Pull e modello di Data-Push

Un client di un moniker asincrono può scegliere tra un modello di pull dei dati e di push dei dati per la Guida di un'operazione di [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrona e la ricezione di notifiche asincrone. Nel modello di pull dei dati il client esegue l'operazione di associazione e il moniker fornisce i dati al client solo quando vengono letti. In altre parole, dopo la prima chiamata a [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), il moniker non fornisce alcun dato al client a meno che il client non abbia utilizzato tutti i dati già disponibili.

Poiché i dati vengono scaricati solo quando vengono richiesti, i client che scelgono il modello di pull dei dati devono assicurarsi di leggere questi dati in modo tempestivo. Nel caso di download di Internet con [moniker URL](url-monikers.md), l'operazione di associazione potrebbe non riuscire se un client è in attesa troppo a lungo prima di richiedere più dati.

Nel modello di push dei dati, il moniker guida l'operazione di associazione asincrona e notifica continuamente al client ogni volta che sono disponibili nuovi dati. Il client può scegliere se leggere i dati in qualsiasi momento durante l'operazione di associazione, ma il moniker guiderà il completamento dell'operazione di associazione, indipendentemente dal fatto che.

Inoltre, è necessario ricordare di seguire le regole COM per l'allocazione di memoria quando si usano moniker asincroni, in particolare quanto segue:

-   Ogni volta che un'interfaccia COM o una chiamata di funzione restituisce un buffer (String o other) al client, il client è responsabile della liberazione della memoria chiamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).
-   Ogni volta che un'interfaccia o una funzione COM richiede un buffer dal client, il client deve allocare il buffer usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) e il chiamato deve liberarlo.

Assicurarsi di seguire queste regole quando si allocano stringhe o buffer passati a moniker asincroni e si ricorda di liberare la memoria restituita dai moniker asincroni. Per informazioni dettagliate, vedere [Managing Memory Allocation](the-com-library.md) and Related topics.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 