---
title: Oggetti collegati e moniker
description: Gli oggetti collegati, ad esempio gli oggetti incorporati, si basano su un gestore di oggetti per comunicare con le applicazioni server.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221936"
---
# <a name="linked-objects-and-monikers"></a>Oggetti collegati e moniker

Gli oggetti collegati, ad esempio gli oggetti incorporati, si basano su un gestore di oggetti per comunicare con le applicazioni server. Tuttavia, l'oggetto collegato gestisce la denominazione e il rilevamento delle origini dei collegamenti. L'oggetto collegato funge da server in-process. Ad esempio, quando attivato, un oggetto collegato individua e avvia l'applicazione server OLE che rappresenta l'origine del collegamento.

Il gestore di un oggetto collegato è costituito da due componenti principali: il componente del gestore e il componente di collegamento. Il componente gestore contiene i componenti di controllo e comunicazione remota e le funzioni in modo molto simile a un gestore per un oggetto incorporato. Il componente di collegamento ha il proprio controller e la propria cache e fornisce l'accesso all'archiviazione strutturata dell'oggetto. Il controller dei componenti di collegamento supporta la denominazione dell'origine tramite l'utilizzo di moniker e l'associazione, il processo di individuazione ed esecuzione dell'origine del collegamento. Per ulteriori informazioni sui moniker e sull'associazione, vedere [la Component Object Model](the-component-object-model.md).

Quando un utente crea inizialmente un oggetto collegato o ne carica uno esistente dalla risorsa di archiviazione, il contenitore carica un'istanza del componente di collegamento in memoria, insieme al gestore dell'oggetto. Il componente di collegamento fornisce le interfacce, in particolare [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), che identificano l'oggetto come collegamento e consentono di gestire la denominazione, il rilevamento e l'aggiornamento dell'origine del collegamento.

Implementando l'interfaccia [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) , un oggetto collegato fornisce il contenitore con funzioni che supportano il collegamento. Solo gli oggetti collegati implementano **IOleLink** e, eseguendo una query per questa interfaccia, un contenitore può determinare se un determinato oggetto è incorporato o collegato. La funzione più importante fornita da **IOleLink** consente a un contenitore di eseguire il binding all'origine dell'oggetto collegato, ovvero per attivare la connessione al documento che archivia i dati nativi dell'oggetto collegato. **IOleLink** definisce anche le funzioni per la gestione delle informazioni sull'oggetto collegato, ad esempio i dati di presentazione memorizzati nella cache e il percorso dell'origine del collegamento.

Quando viene salvato un documento composto contenente un oggetto collegato, i dati del collegamento vengono salvati con l'origine del collegamento, non con il contenitore. Insieme al documento composto vengono salvate solo le informazioni relative al nome e alla posizione. Questo comportamento è contrario a quello di un oggetto incorporato, i cui dati vengono archiviati insieme a quello del relativo contenitore.

Le applicazioni contenitore possono fornire informazioni sui rispettivi oggetti incorporati in modo che quest'ultima, o parti di esso, possano fungere da origini di collegamento. Implementando il supporto per il collegamento agli oggetti incorporati del contenitore, si rendono possibili gli incorporamenti nidificati, evitando all'utente di dover tenere traccia degli originali di ogni oggetto di incorporamento a cui si desidera un collegamento. Se, ad esempio, un utente vuole incorporare un foglio di lavoro di Microsoft Excel in Microsoft Word e il foglio di lavoro contiene una bitmap creata in un pennello, l'utente può collegarsi a una copia della bitmap contenuta nel foglio di lavoro anziché all'originale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> <dt>

[Gestori di oggetti](object-handlers.md)
</dt> </dl>

 

 




