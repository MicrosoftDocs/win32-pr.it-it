---
title: Limite di tempo di ricerca
description: Quando si richiede una ricerca in un server con un carico di lavoro elevato, è possibile indicare al server di limitare la ricerca a un limite di tempo specificato.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Limite di tempo di ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690516"
---
# <a name="search-time-limit"></a>Limite di tempo di ricerca

Quando si richiede una ricerca in un server con un carico di lavoro elevato, è possibile indicare al server di limitare la ricerca a un limite di tempo specificato. Ad esempio, per eseguire un'applicazione per generare un report settimanale in un server che sta eseguendo quasi la capacità e per evitare di ottimizzare il tempo di CPU e impedire l'esecuzione di altri processi, è possibile impostare il tempo di ricerca su un valore ridotto ed eseguire nuovamente l'applicazione in un secondo momento se non riesce a generare il report.

Alcuni server possono imporre un proprio limite di tempo amministrativo. In questi casi, se si specifica un valore di limite di tempo di ricerca maggiore del limite di tempo amministrativo, il server ignora la specifica e usa invece il limite di tempo amministrativo interno.

Per altre informazioni sull'uso dell'opzione search time limit con un'interfaccia di ricerca specifica, vedere:

-   [Limite di tempo del server con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




