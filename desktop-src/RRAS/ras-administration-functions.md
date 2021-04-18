---
title: Funzioni di amministrazione RAS
description: In questa documentazione vengono descritte le funzioni RRAS utilizzate per sviluppare software per amministrare le connessioni remote RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332044"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="0115c-103">Funzioni di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="0115c-103">RAS Administration Functions</span></span>

<span data-ttu-id="0115c-104">In questa documentazione vengono descritte le funzioni RRAS utilizzate per sviluppare software per amministrare le connessioni remote RAS.</span><span class="sxs-lookup"><span data-stu-id="0115c-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="0115c-105">Queste funzioni includono:</span><span class="sxs-lookup"><span data-stu-id="0115c-105">These functions include:</span></span>

-   [<span data-ttu-id="0115c-106">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="0115c-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="0115c-107">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="0115c-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="0115c-108">**MprAdminConnectionEnumEx**</span><span class="sxs-lookup"><span data-stu-id="0115c-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="0115c-109">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0115c-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="0115c-110">**MprAdminConnectionGetInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0115c-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="0115c-111">**MprAdminConnectionRemoveQuarantine**</span><span class="sxs-lookup"><span data-stu-id="0115c-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="0115c-112">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="0115c-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="0115c-113">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0115c-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="0115c-114">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="0115c-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="0115c-115">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0115c-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="0115c-116">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="0115c-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="0115c-117">Funzioni aggiuntive vengono usate per l'amministrazione RAS e il router.</span><span class="sxs-lookup"><span data-stu-id="0115c-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="0115c-118">Le funzioni seguenti sono documentate nelle informazioni di riferimento sulle [funzioni di amministrazione del router](router-administration-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="0115c-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="0115c-119">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="0115c-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="0115c-120">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="0115c-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="0115c-121">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="0115c-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="0115c-122">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="0115c-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="0115c-123">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0115c-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="0115c-124">Per implementare una DLL di amministrazione RAS, utilizzare le funzioni descritte nell'argomento seguente:</span><span class="sxs-lookup"><span data-stu-id="0115c-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="0115c-125">Funzioni DLL amministratore RAS</span><span class="sxs-lookup"><span data-stu-id="0115c-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="0115c-126">Per gestire gli utenti di un server RAS, utilizzare le funzioni descritte nell'argomento seguente:</span><span class="sxs-lookup"><span data-stu-id="0115c-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="0115c-127">Funzioni di amministrazione utenti RAS</span><span class="sxs-lookup"><span data-stu-id="0115c-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




