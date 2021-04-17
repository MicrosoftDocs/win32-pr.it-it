---
description: L'interfaccia IDownloadJob definisce i metodi seguenti.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Metodi IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526701"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="d0167-103">Metodi IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="d0167-103">IDownloadJob Methods</span></span>

<span data-ttu-id="d0167-104">L'interfaccia [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0167-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="d0167-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="d0167-105">Method</span></span>                                            | <span data-ttu-id="d0167-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0167-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0167-107">**Pulizia**</span><span class="sxs-lookup"><span data-stu-id="d0167-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="d0167-108">Attende il completamento di un'operazione asincrona e rilascia tutti i callback.</span><span class="sxs-lookup"><span data-stu-id="d0167-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="d0167-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="d0167-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="d0167-110">Restituisce un'interfaccia [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) che descrive lo stato di avanzamento corrente di un download.</span><span class="sxs-lookup"><span data-stu-id="d0167-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="d0167-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="d0167-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="d0167-112">Esegue una richiesta per terminare un download asincrono.</span><span class="sxs-lookup"><span data-stu-id="d0167-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



