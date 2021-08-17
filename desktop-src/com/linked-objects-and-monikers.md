---
title: Oggetti collegati e moniker
description: Gli oggetti collegati, come gli oggetti incorporati, si basano su un gestore di oggetti per comunicare con le applicazioni server.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb8107a5c98ae407cc8e6198d782f75b092110232ae23f41a42dcaefae31758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736494"
---
# <a name="linked-objects-and-monikers"></a>Oggetti collegati e moniker

Gli oggetti collegati, come gli oggetti incorporati, si basano su un gestore di oggetti per comunicare con le applicazioni server. L'oggetto collegato stesso, tuttavia, gestisce la denominazione e il rilevamento delle origini dei collegamenti. L'oggetto collegato funge da server in-process. Ad esempio, se attivato, un oggetto collegato individua e avvia l'applicazione server OLE che rappresenta l'origine del collegamento.

Il gestore di un oggetto collegato è costituito da due componenti principali: il componente gestore e il componente di collegamento. Il componente gestore contiene le parti e le funzioni di controllo e comunicazione remota in modo molto simile a un gestore per un oggetto incorporato. Il componente di collegamento ha un proprio controller e una propria cache e fornisce l'accesso all'archiviazione strutturata dell'oggetto. Il controller dei componenti di collegamento supporta la denominazione dell'origine tramite l'uso di moniker e l'associazione, il processo di individuazione ed esecuzione dell'origine del collegamento. Per altre informazioni sui moniker e sull'associazione, [vedere l'Component Object Model](the-component-object-model.md).

Quando un utente crea inizialmente un oggetto collegato o ne carica uno esistente dalla memoria, il contenitore carica un'istanza del componente di collegamento in memoria, insieme al gestore dell'oggetto . Il componente di collegamento fornisce interfacce, in particolare [**IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)che identificano l'oggetto come collegamento e lo consentono di gestire la denominazione, il rilevamento e l'aggiornamento dell'origine del collegamento.

Implementando [**l'interfaccia IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) un oggetto collegato fornisce al relativo contenitore funzioni che supportano il collegamento. Solo gli oggetti collegati **implementano IOleLink** e, tramite una query per questa interfaccia, un contenitore può determinare se un determinato oggetto è incorporato o collegato. La funzione più importante fornita da **IOleLink** consente a un contenitore di eseguire il binding all'origine dell'oggetto collegato, ad esempio per attivare la connessione al documento in cui sono archiviati i dati nativi dell'oggetto collegato. **IOleLink definisce** anche le funzioni per la gestione delle informazioni sull'oggetto collegato, ad esempio i dati di presentazione memorizzati nella cache e il percorso dell'origine del collegamento.

Quando viene salvato un documento composto contenente un oggetto collegato, i dati del collegamento vengono salvati con l'origine del collegamento, non con il contenitore. Insieme al documento composto vengono salvate solo le informazioni relative al nome e al percorso. Questo comportamento è diverso da quello di un oggetto incorporato, i cui dati vengono archiviati insieme a quello del relativo contenitore.

Le applicazioni contenitore possono fornire informazioni sui relativi oggetti incorporati in modo che quest'ultimo, o parti di tali oggetti, possa fungere da origini di collegamento. Implementando il supporto per il collegamento agli oggetti incorporati del contenitore, si rendono possibili incorporamenti annidati, senza dover tenere traccia degli originali di ogni oggetto di incorporamento a cui si desidera un collegamento. Ad esempio, se un utente vuole incorporare un foglio di lavoro di Microsoft Excel in Microsoft Word e il foglio di lavoro contiene una bitmap creata in Paintbrush, l'utente può collegarsi a una copia della bitmap contenuta nel foglio di lavoro anziché all'originale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> <dt>

[Gestori di oggetti](object-handlers.md)
</dt> </dl>

 

 




