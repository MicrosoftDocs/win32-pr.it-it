---
description: L'interfaccia IInstallationJob definisce i metodi seguenti.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Metodi IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129651"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="ca880-103">Metodi IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="ca880-103">IInstallationJob Methods</span></span>

<span data-ttu-id="ca880-104">L'interfaccia [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca880-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="ca880-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="ca880-105">Method</span></span>                                                | <span data-ttu-id="ca880-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca880-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca880-107">**Pulizia**</span><span class="sxs-lookup"><span data-stu-id="ca880-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="ca880-108">Attende il completamento di un'operazione asincrona, quindi rilascia tutti i callback.</span><span class="sxs-lookup"><span data-stu-id="ca880-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="ca880-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="ca880-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="ca880-110">Restituisce un'interfaccia [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) che descrive lo stato di avanzamento corrente di un'installazione o di una disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="ca880-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="ca880-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="ca880-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="ca880-112">Esegue una richiesta per annullare l'installazione o la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="ca880-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



