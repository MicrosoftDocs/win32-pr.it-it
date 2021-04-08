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
# <a name="database-import-and-export"></a><span data-ttu-id="7e7ce-103">Importazione ed esportazione di database</span><span class="sxs-lookup"><span data-stu-id="7e7ce-103">Database Import and Export</span></span>

<span data-ttu-id="7e7ce-104">Quando si utilizza il Peer Graphing o le infrastrutture di raggruppamento peer, le informazioni (record) pubblicate dai peer in un grafico o gruppo vengono archiviate come database in ogni computer peer.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="7e7ce-105">Per eseguire la migrazione di un'applicazione da un computer a un altro, è possibile esportare un peer Graphing o un database di raggruppamento peer da un computer e quindi importarlo in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="7e7ce-106">Nell'elenco seguente vengono identificate informazioni importanti sull'utilizzo dei database:</span><span class="sxs-lookup"><span data-stu-id="7e7ce-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="7e7ce-107">È possibile importare solo un database con lo stesso grafico e ID peer.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="7e7ce-108">Non è possibile chiamare le funzioni di importazione ed esportazione se [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) sono stati chiamati.</span><span class="sxs-lookup"><span data-stu-id="7e7ce-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="7e7ce-109">L' **infrastruttura di Peer Graphing** usa le chiamate seguenti per importare ed esportare un database di record:</span><span class="sxs-lookup"><span data-stu-id="7e7ce-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="7e7ce-110">**PeerGraphExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="7e7ce-111">**PeerGraphImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="7e7ce-112">L' **infrastruttura di raggruppamento peer** utilizza le seguenti chiamate per importare ed esportare un database di record:</span><span class="sxs-lookup"><span data-stu-id="7e7ce-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="7e7ce-113">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="7e7ce-114">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7e7ce-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



