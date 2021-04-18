---
title: Limite tempo di ricerca
description: Quando si richiede una ricerca in un server con un carico di lavoro elevato, è consigliabile indicare al server di limitare la ricerca a un limite di tempo specificato.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Limite tempo di ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297653"
---
# <a name="search-time-limit"></a>Limite tempo di ricerca

Quando si richiede una ricerca in un server con un carico di lavoro elevato, è consigliabile indicare al server di limitare la ricerca a un limite di tempo specificato. Per eseguire, ad esempio, un'applicazione per generare un report settimanale su un server in cui è in esecuzione near Capacity e per evitare di massimizzare il tempo della CPU e impedire l'esecuzione di altri processi, è possibile impostare il tempo di ricerca su un valore ridotto ed eseguire nuovamente l'applicazione in un secondo momento se non riesce a generare il report.

Alcuni server possono imporre un limite di tempo amministrativo. In questi casi, se si specifica un valore per il limite di tempo di ricerca superiore al limite di tempo amministrativo, il server ignora la specifica e usa il limite di tempo amministrativo interno.

Per ulteriori informazioni sull'utilizzo dell'opzione per il limite di tempo di ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Limite di tempo del server con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




