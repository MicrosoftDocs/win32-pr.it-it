---
description: Nell'elenco seguente sono inclusi i metodi CMSPStream chiamati dall'oggetto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Metodi CMSPStream chiamati dall'oggetto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314625"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="a0250-103">Metodi pubblici CMSPStream chiamati dall'oggetto MSPCall</span><span class="sxs-lookup"><span data-stu-id="a0250-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="a0250-104">Metodi pubblici CMSPStream</span><span class="sxs-lookup"><span data-stu-id="a0250-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="a0250-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0250-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0250-106">**Init**</span><span class="sxs-lookup"><span data-stu-id="a0250-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="a0250-107">Chiamato da **MSPCall** quando viene creato il flusso.</span><span class="sxs-lookup"><span data-stu-id="a0250-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="a0250-108">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="a0250-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="a0250-109">Chiamato da **MSPCall** per deselezionare tutti gli oggetti Terminal e rilasciare l'oggetto call.</span><span class="sxs-lookup"><span data-stu-id="a0250-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="a0250-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="a0250-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="a0250-111">Chiamato dall'oggetto MSPCall per ottenere lo stato corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="a0250-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="a0250-112">**HandleTSPData**</span><span class="sxs-lookup"><span data-stu-id="a0250-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="a0250-113">L'oggetto chiamata derivato può chiamare questo metodo per consentire al flusso di gestire i comandi del TSP.</span><span class="sxs-lookup"><span data-stu-id="a0250-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="a0250-114">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="a0250-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="a0250-115">Chiamato dall'oggetto MSPCall per consentire al flusso di gestire gli eventi del grafo.</span><span class="sxs-lookup"><span data-stu-id="a0250-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



