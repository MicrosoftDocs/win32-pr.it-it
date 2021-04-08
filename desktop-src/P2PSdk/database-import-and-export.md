---
description: Quando si utilizza il Peer Graphing o le infrastrutture di raggruppamento peer, le informazioni (record) pubblicate dai peer in un grafico o gruppo vengono archiviate come database in ogni computer peer.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importazione ed esportazione di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967540"
---
# <a name="database-import-and-export"></a>Importazione ed esportazione di database

Quando si utilizza il Peer Graphing o le infrastrutture di raggruppamento peer, le informazioni (record) pubblicate dai peer in un grafico o gruppo vengono archiviate come database in ogni computer peer. Per eseguire la migrazione di un'applicazione da un computer a un altro, è possibile esportare un peer Graphing o un database di raggruppamento peer da un computer e quindi importarlo in un altro computer.

Nell'elenco seguente vengono identificate informazioni importanti sull'utilizzo dei database:

-   È possibile importare solo un database con lo stesso grafico e ID peer.
-   Non è possibile chiamare le funzioni di importazione ed esportazione se [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) sono stati chiamati.

L' **infrastruttura di Peer Graphing** usa le chiamate seguenti per importare ed esportare un database di record:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

L' **infrastruttura di raggruppamento peer** utilizza le seguenti chiamate per importare ed esportare un database di record:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



