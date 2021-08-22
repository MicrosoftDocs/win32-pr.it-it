---
title: Timeout della ricerca
description: Un client può anche imporre un limite di tempo che attende che un server restituirà il set di risultati.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Timeout della ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99b287c1bc0ba0da5e39b579c4a454eae821cf2c443930a5ae0376412e2c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082305"
---
# <a name="search-time-out"></a>Timeout della ricerca

Un client può anche imporre un limite di tempo che attende che un server restituirà il set di risultati. Il valore dell'opzione "timeout ricerca" specifica questo limite. Quando il server non risponde a una query entro il periodo di tempo specificato, il client può arrestare la ricerca e riprovare in un secondo momento.

La proprietà di timeout è utile quando un client richiede una ricerca asincrona. In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività durante l'attesa che il server restituirà i risultati. È possibile che il server possa passare offline senza inviare una notifica al client. In questo caso, il client non è in grado di riconoscere che il server sta ancora elaborando la query o se ha smesso di essere in tempo reale. La proprietà di timeout fornisce al client un controllo in tali istanze.

Per altre informazioni sull'uso dell'opzione di timeout della ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Limite di tempo del client con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




