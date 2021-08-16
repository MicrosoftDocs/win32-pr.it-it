---
title: Caching risultato (lato client)
description: La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria client, offrendo miglioramenti delle prestazioni per il lato client.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Caching risultato (lato client) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2394c4f9e3213261bc52e15ada6fa9416703706fedeccaf144493821133e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840501"
---
# <a name="caching-the-result-client-side"></a>Caching risultato (lato client)

La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria client, offrendo miglioramenti delle prestazioni per il lato client. Un client può rivedere ripetutamente un oggetto senza più corse al server. Per impostazione predefinita, ADSI memorizza nella cache il set di risultati per i client. Ciò consente ad ADSI di fornire ai client SQL cursore simile a quello di . È possibile scorrere più volte un determinato set di risultati.

ADSI consente inoltre ai client di disattivare la cache per ridurre i requisiti di memoria. Se la memorizzazione nella cache sul lato client è disabilitata, il client non mantiene il set di risultati in memoria. Ogni riga viene liberata dopo che è stata recuperata dall'applicazione. La disabilitazione della memorizzazione nella cache sul lato client può essere utile per ridurre i requisiti di memoria sul lato client, ad esempio quando si prevede di eseguire un solo passaggio attraverso il set di risultati. Tuttavia, quando i client sceglie di non memorizzare nella cache il risultato, non supportano il cursore.

Per altre informazioni sulla memorizzazione nella cache dei risultati con un'interfaccia di ricerca specifica, vedere:

-   [Risultati Caching con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




