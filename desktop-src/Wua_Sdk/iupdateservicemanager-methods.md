---
description: L'interfaccia IUpdateServiceManager definisce i metodi seguenti.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Metodi IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525086"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="f3de1-103">Metodi IUpdateServiceManager</span><span class="sxs-lookup"><span data-stu-id="f3de1-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="f3de1-104">L'interfaccia [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3de1-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="f3de1-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3de1-105">Method</span></span>                                                                           | <span data-ttu-id="f3de1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3de1-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3de1-107">**AddScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="f3de1-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="f3de1-108">Registra un pacchetto di analisi come servizio con Windows Update Agent (WUA) e quindi restituisce un'interfaccia [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .</span><span class="sxs-lookup"><span data-stu-id="f3de1-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="f3de1-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="f3de1-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="f3de1-110">Registra un servizio con WUA.</span><span class="sxs-lookup"><span data-stu-id="f3de1-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="f3de1-111">**RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="f3de1-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="f3de1-112">Registra un servizio con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="f3de1-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="f3de1-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="f3de1-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="f3de1-114">Rimuove una registrazione del servizio da WUA.</span><span class="sxs-lookup"><span data-stu-id="f3de1-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="f3de1-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="f3de1-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="f3de1-116">Imposta le opzioni per l'oggetto che specifica l'ID del servizio e indica se visualizzare un avviso quando si modifica la registrazione del Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="f3de1-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="f3de1-117">**UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="f3de1-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="f3de1-118">Annulla la registrazione di un servizio con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="f3de1-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



