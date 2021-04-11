---
description: L'interfaccia IUpdateSession3 definisce i metodi seguenti.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Metodi IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128275"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="7f881-103">Metodi IUpdateSession3</span><span class="sxs-lookup"><span data-stu-id="7f881-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="7f881-104">L'interfaccia [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f881-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="7f881-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="7f881-105">Method</span></span>                                                                           | <span data-ttu-id="7f881-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f881-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f881-107">**CreateUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="7f881-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="7f881-108">Restituisce un puntatore a un'interfaccia [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) per la sessione.</span><span class="sxs-lookup"><span data-stu-id="7f881-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="7f881-109">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="7f881-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="7f881-110">Restituisce un puntatore a un'interfaccia [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) .</span><span class="sxs-lookup"><span data-stu-id="7f881-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="7f881-111">L'interfaccia contiene i record degli eventi corrispondenti nel computer.</span><span class="sxs-lookup"><span data-stu-id="7f881-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="7f881-112">In questo modo, il metodo [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) esegue una query in modo sincrono sul computer per la cronologia degli eventi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7f881-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="7f881-113">Per informazioni sui membri ereditati da questa interfaccia, vedere le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f881-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="7f881-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="7f881-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="7f881-115">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="7f881-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



