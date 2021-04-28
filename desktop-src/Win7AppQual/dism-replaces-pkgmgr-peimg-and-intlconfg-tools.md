---
description: Gestione e manutenzione immagini distribuzione
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestione e manutenzione immagini distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088489"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="0b5e0-103">Gestione e manutenzione immagini distribuzione</span><span class="sxs-lookup"><span data-stu-id="0b5e0-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0b5e0-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="0b5e0-104">Affected Platforms</span></span>

<span data-ttu-id="0b5e0-105">**Client** - Windows Vista SP1 e versioni successive \| windows 7</span><span class="sxs-lookup"><span data-stu-id="0b5e0-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="0b5e0-106">**Server** - Windows Server 2008 RTM e versioni successive \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b5e0-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="0b5e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b5e0-107">Description</span></span>

<span data-ttu-id="0b5e0-108">Lo Gestione e manutenzione immagini distribuzione (DISM) sostituisce gli strumenti pkgmgr, PEImg e IntlConfg ritirati in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="0b5e0-109">Gestione e manutenzione immagini distribuzione offre un unico strumento centralizzato per eseguire tutte le funzioni di questi tre strumenti in modo più efficiente e standardizzato, eliminando la fonte di molte delle frustrazioni riscontrate dagli attuali utenti di questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="0b5e0-110">Gestione e manutenzione immagini distribuzione include uno shim per Windows Vista SP1 e versioni successive, nonché per Windows Server 2008 RTM e versioni successive, che reindirizza le chiamate pkgmgr da applicazioni legacy in esecuzione in Windows 7 a Gestione e manutenzione immagini distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="0b5e0-111">Se l'applicazione è in esecuzione in uno dei sistemi operativi supportati, lo shim instrada la chiamata a pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="0b5e0-112">Non esistono s shims per le applicazioni legacy che chiamano PEImg o IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="0b5e0-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0b5e0-113">Usage</span></span>

<span data-ttu-id="0b5e0-114">Gestione e manutenzione immagini distribuzione è trasparente per gli utenti finali di pkgmgr in una delle piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="0b5e0-115">Tuttavia, se un'applicazione chiama PEImg o IntlConfg da Windows 7, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="0b5e0-116">Aggiornare gli script che chiamano pkgmgr, PEImg o IntlConfg per chiamare invece Gestione e manutenzione immagini distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="0b5e0-117">È importante includere l'aggiornamento degli script pkgmgr in questo sforzo, poiché lo shim che fornisce la compatibilità con le versioni precedenti per pkgmgr verrà rimosso nelle versioni future dei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="0b5e0-118">Verificare che le chiamate a Gestione e manutenzione immagini distribuzione siano state sostituite da qualsiasi chiamata a pkgmgr, PEImg e IntlConfg e che l'operazione sia stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b5e0-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b5e0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b5e0-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0b5e0-120">[Gestione e manutenzione immagini distribuzione (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0b5e0-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
