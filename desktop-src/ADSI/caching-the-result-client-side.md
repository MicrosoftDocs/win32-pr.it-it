---
title: Memorizzazione dei risultati nella cache (lato client)
description: La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria del client, fornendo miglioramenti delle prestazioni per il lato client.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Memorizzazione nella cache del risultato (lato client) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955109"
---
# <a name="caching-the-result-client-side"></a>Memorizzazione dei risultati nella cache (lato client)

La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria del client, fornendo miglioramenti delle prestazioni per il lato client. Un client può rivedere ripetutamente un oggetto senza più corse al server. Per impostazione predefinita, ADSI memorizza nella cache il set di risultati per i client. In questo modo, ADSI fornisce ai client il supporto del cursore simile a SQL. È possibile scorrere più volte un determinato set di risultati.

ADSI consente inoltre ai client di disattivare la cache per ridurre i requisiti di memoria. Se la memorizzazione nella cache sul lato client è disabilitata, il client non mantiene il set di risultati in memoria. Ogni riga viene liberata dopo che è stata recuperata dall'applicazione. La disabilitazione della memorizzazione nella cache sul lato client può essere utile per ridurre i requisiti di memoria sul lato client in questi casi, ad esempio quando si prevede di eseguire un solo passaggio attraverso il set di risultati. Tuttavia, quando i client scelgono di non memorizzare nella cache il risultato, rinunciano al supporto del cursore.

Per ulteriori informazioni sulla memorizzazione nella cache dei risultati con un'interfaccia di ricerca specifica, vedere:

-   [Caching dei risultati con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




