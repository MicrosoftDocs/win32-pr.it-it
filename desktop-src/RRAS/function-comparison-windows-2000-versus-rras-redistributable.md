---
title: Confronto tra le funzioni di Windows 2000 e RRAS ridistribuibile
description: L'API RAS viene distribuita come funzionalità di Windows 2000 e sistemi operativi successivi ed è disponibile come ridistribuibile per Windows NT 4,0 con Service Pack 3 (SP3) e versioni precedenti.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298943"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="566e4-103">Confronto tra le funzioni: Windows 2000 e RRAS ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="566e4-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="566e4-104">L'API RAS viene distribuita come funzionalità di Windows 2000 e sistemi operativi successivi ed è disponibile come ridistribuibile per Windows NT 4,0 con Service Pack 3 (SP3) e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="566e4-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="566e4-105">RAS fornisce le stesse funzionalità in entrambi i formati, ma la convenzione di denominazione utilizzata è diversa per gli elementi di riferimento in ogni versione dell'API RAS.</span><span class="sxs-lookup"><span data-stu-id="566e4-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="566e4-106">Le funzioni RAS per Windows NT 4,0 con SP3 e versioni precedenti iniziano in genere con il prefisso "RasAdmin".</span><span class="sxs-lookup"><span data-stu-id="566e4-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="566e4-107">Le funzioni analoghe per il servizio Routing e accesso remoto (RRAS) iniziano con il prefisso "MprAdmin".</span><span class="sxs-lookup"><span data-stu-id="566e4-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="566e4-108">Ad esempio, RAS fornisce una funzione denominata [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span><span class="sxs-lookup"><span data-stu-id="566e4-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="566e4-109">La funzione analoga in RRAS è denominata [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="566e4-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="566e4-110">Come esempio simile, RAS fornisce la funzione di callback [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="566e4-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="566e4-111">RRAS fornisce una funzione di callback simile denominata [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="566e4-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="566e4-112">Le eccezioni a questa regola sono [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), che in RRAS è [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)e [**RasAdminFreeBuffer**](rasadminfreebuffer.md), che in RRAS è [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span><span class="sxs-lookup"><span data-stu-id="566e4-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="566e4-113">Nella tabella seguente sono elencate le funzioni RAS di Windows NT 4,0 SP3 e le funzioni RRAS corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="566e4-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="566e4-114">RAS di Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="566e4-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="566e4-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="566e4-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="566e4-116">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="566e4-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="566e4-117">**MprAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="566e4-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="566e4-118">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="566e4-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="566e4-119">**MprAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="566e4-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="566e4-120">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="566e4-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="566e4-121">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="566e4-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="566e4-122">**RasAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="566e4-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="566e4-123">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="566e4-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="566e4-124">**RasAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="566e4-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="566e4-125">**MprAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="566e4-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="566e4-126">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="566e4-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="566e4-127">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="566e4-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="566e4-128">**RasAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="566e4-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="566e4-129">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="566e4-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="566e4-130">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="566e4-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="566e4-131">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="566e4-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="566e4-132">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="566e4-133">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="566e4-134">**RasAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="566e4-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="566e4-135">**MprAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="566e4-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="566e4-136">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="566e4-137">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="566e4-138">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="566e4-139">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="566e4-140">Sebbene le funzioni RRAS siano simili a quelle di Windows NT 4,0 con SP3 e le controparti RAS precedenti nella funzionalità, le funzioni RRAS utilizzano spesso un set di parametri diverso.</span><span class="sxs-lookup"><span data-stu-id="566e4-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="566e4-141">Per informazioni complete sull'elenco di parametri di questa funzione, vedere la pagina di riferimento relativa a una determinata funzione.</span><span class="sxs-lookup"><span data-stu-id="566e4-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="566e4-142">RRAS Redistributable per Windows NT 4,0 con SP3 e versioni precedenti aggiunge le funzioni seguenti, che non hanno controparti RAS:</span><span class="sxs-lookup"><span data-stu-id="566e4-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="566e4-143">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="566e4-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="566e4-144">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="566e4-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="566e4-145">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="566e4-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="566e4-146">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="566e4-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="566e4-147">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="566e4-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="566e4-148">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="566e4-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="566e4-149">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="566e4-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="566e4-150">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="566e4-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="566e4-151">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="566e4-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="566e4-152">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="566e4-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="566e4-153">Oltre alle funzioni precedenti, Windows 2000 e i sistemi operativi successivi aggiungono le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="566e4-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="566e4-154">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="566e4-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="566e4-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="566e4-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="566e4-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="566e4-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




