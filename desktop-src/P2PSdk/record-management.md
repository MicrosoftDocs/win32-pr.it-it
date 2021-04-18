---
description: Per gestire i record, è possibile utilizzare le informazioni archiviate in \_ strutture di record peer.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestione dei record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314739"
---
# <a name="record-management"></a><span data-ttu-id="b4fe8-103">Gestione dei record</span><span class="sxs-lookup"><span data-stu-id="b4fe8-103">Record Management</span></span>

<span data-ttu-id="b4fe8-104">Per gestire i record, è possibile utilizzare le informazioni archiviate in strutture di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="b4fe8-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="b4fe8-105">Quando i record vengono creati, aggiornati o eliminati, le modifiche apportate a un grafo vengono replicate in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="b4fe8-106">Nella tabella seguente vengono identificate le regole per l'aggiornamento e l'aggiornamento automatico dei record.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="b4fe8-107">Attività di gestione</span><span class="sxs-lookup"><span data-stu-id="b4fe8-107">Management Task</span></span>     | <span data-ttu-id="b4fe8-108">Regola</span><span class="sxs-lookup"><span data-stu-id="b4fe8-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fe8-109">Aggiornamento di un record</span><span class="sxs-lookup"><span data-stu-id="b4fe8-109">Updating a record</span></span>   | <span data-ttu-id="b4fe8-110">Mantenerne lo stesso tempo o aumentarlo.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="b4fe8-111">Non è possibile ridurre l'ora di scadenza.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="b4fe8-112">Aggiornamento di un record</span><span class="sxs-lookup"><span data-stu-id="b4fe8-112">Refreshing a record</span></span> | <span data-ttu-id="b4fe8-113">Usare il flag di aggiornamento automatico del [**\_ flag di record \_ \_ peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) per aggiornare automaticamente un record.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="b4fe8-114">Utilizzare questo flag solo quando il nodo che pubblica un record è online.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="b4fe8-115">In caso contrario, non usare questo flag.</span><span class="sxs-lookup"><span data-stu-id="b4fe8-115">Otherwise, do not use this flag.</span></span> |



 

 

 



