---
description: Quando si usa peer graphing o le infrastrutture di raggruppamento peer, le informazioni (record) che i peer pubblicano in un grafo o in un gruppo vengono archiviate come database in ogni computer peer.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importazione ed esportazione di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc047e6f58c7aeab07f6d13f8f7364f3f2f1191e50320513bc153e34c4c042c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979061"
---
# <a name="database-import-and-export"></a>Importazione ed esportazione di database

Quando si usa peer graphing o le infrastrutture di raggruppamento peer, le informazioni (record) che i peer pubblicano in un grafo o in un gruppo vengono archiviate come database in ogni computer peer. Per eseguire la migrazione di un'applicazione da un computer a un altro, è possibile esportare un database peer graphing o di raggruppamento peer da un computer e quindi importarlo in un altro.

L'elenco seguente identifica informazioni importanti sull'uso dei database:

-   È possibile importare solo un database con lo stesso grafo e lo stesso ID peer.
-   Non è possibile chiamare le funzioni di importazione ed esportazione se sono stati chiamati [**PeerGraphListen,**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect.**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)

**Peer Graphing Infrastructure usa** le chiamate seguenti per importare ed esportare un database di record:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

**L'infrastruttura di raggruppamento** peer usa le chiamate seguenti per importare ed esportare un database di record:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



