---
title: Funzioni di interfaccia del router
description: Usare le funzioni seguenti per amministrare le interfacce sul router.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328231"
---
# <a name="router-interface-functions"></a><span data-ttu-id="508f9-103">Funzioni di interfaccia del router</span><span class="sxs-lookup"><span data-stu-id="508f9-103">Router Interface Functions</span></span>

<span data-ttu-id="508f9-104">Usare le funzioni seguenti per amministrare le interfacce sul router.</span><span class="sxs-lookup"><span data-stu-id="508f9-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="508f9-105">Funzione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="508f9-105">Administration Function</span></span>                                          | <span data-ttu-id="508f9-106">Funzione di configurazione</span><span class="sxs-lookup"><span data-stu-id="508f9-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="508f9-107">**MprAdminInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="508f9-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="508f9-108">**MprConfigInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="508f9-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="508f9-109">**MprAdminInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="508f9-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="508f9-110">**MprConfigInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="508f9-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="508f9-111">**MprAdminInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="508f9-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="508f9-112">**MprConfigInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="508f9-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="508f9-113">**MprAdminInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="508f9-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="508f9-114">**MprConfigInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="508f9-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="508f9-115">**MprAdminInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="508f9-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="508f9-116">**MprConfigInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="508f9-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="508f9-117">**MprAdminInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="508f9-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="508f9-118">**MprConfigInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="508f9-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="508f9-119">Queste funzioni influiscono sulle interfacce stesse, non sui client in esecuzione sulle interfacce.</span><span class="sxs-lookup"><span data-stu-id="508f9-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="508f9-120">Per questo motivo, nessuna delle funzioni richiede che il chiamante specifichi un trasporto specifico (IP o IPX); Sebbene i client, ad esempio i protocolli di routing, siano associati a trasporti particolari, le interfacce non lo sono.</span><span class="sxs-lookup"><span data-stu-id="508f9-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="508f9-121">Queste funzioni vengono gestite direttamente da DIM.</span><span class="sxs-lookup"><span data-stu-id="508f9-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="508f9-122">Non utilizzano i gestori dei router.</span><span class="sxs-lookup"><span data-stu-id="508f9-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="508f9-123">Le funzioni [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) non possono creare o eliminare interfacce LAN.</span><span class="sxs-lookup"><span data-stu-id="508f9-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="508f9-124">Possono solo creare o eliminare le interfacce di connessione a richiesta.</span><span class="sxs-lookup"><span data-stu-id="508f9-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="508f9-125">Vedere [**\_ \_ tipo di interfaccia del router**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) per un elenco di tipi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="508f9-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




