---
title: Timeout della ricerca
description: Un client può inoltre imporre un limite di tempo che attende che un server restituisca il set di risultati.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Timeout della ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328359"
---
# <a name="search-time-out"></a>Timeout della ricerca

Un client può inoltre imporre un limite di tempo che attende che un server restituisca il set di risultati. Il valore dell'opzione "timeout di ricerca" specifica questo limite. Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può arrestare la ricerca e riprovare più tardi.

La proprietà di timeout è utile quando un client richiede una ricerca asincrona. In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività in attesa che il server restituisca i risultati. È possibile che il server sia offline senza notificare al client. In questo caso, il client non è in grado di riconoscere che il server sta ancora elaborando la query o se è stata interrotta. La proprietà di timeout fornisce al client un controllo in tali istanze.

Per ulteriori informazioni sull'utilizzo dell'opzione di timeout di ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Limite di tempo client con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 




