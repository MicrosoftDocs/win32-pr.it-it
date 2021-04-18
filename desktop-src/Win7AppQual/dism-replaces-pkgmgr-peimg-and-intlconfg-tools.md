---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestione e manutenzione immagini distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318579"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="ad80f-103">Gestione e manutenzione immagini distribuzione</span><span class="sxs-lookup"><span data-stu-id="ad80f-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ad80f-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="ad80f-104">Affected Platforms</span></span>

<span data-ttu-id="ad80f-105">**Client** -Windows Vista SP1 e versioni successive \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad80f-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="ad80f-106">**Server** : windows Server 2008 RTM e versioni successive \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad80f-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="ad80f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad80f-107">Description</span></span>

<span data-ttu-id="ad80f-108">Lo strumento Gestione e manutenzione immagini distribuzione (DISM) sostituisce gli strumenti pkgmgr, PEImg e IntlConfg che vengono ritirati in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad80f-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="ad80f-109">DISM fornisce un unico strumento centralizzato per l'esecuzione di tutte le funzioni di questi tre strumenti in modo più efficiente e standardizzato, eliminando l'origine di molte delle frustrazioni riscontrate dagli utenti correnti di questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="ad80f-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="ad80f-110">DISM include uno shim per Windows Vista SP1 e versioni successive, nonché per Windows Server 2008 RTM e versioni successive, che reindirizza le chiamate pkgmgr da applicazioni legacy in esecuzione su Windows 7 a DISM.</span><span class="sxs-lookup"><span data-stu-id="ad80f-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="ad80f-111">Se l'applicazione è in esecuzione in uno dei sistemi operativi supportati, lo shim instrada la chiamata a pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="ad80f-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="ad80f-112">Non esistono shim per le applicazioni legacy che chiamano PEImg o IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="ad80f-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="ad80f-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ad80f-113">Usage</span></span>

<span data-ttu-id="ad80f-114">DISM è trasparente per gli utenti finali di pkgmgr su qualsiasi piattaforma supportata.</span><span class="sxs-lookup"><span data-stu-id="ad80f-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="ad80f-115">Tuttavia, se un'applicazione chiama PEImg o IntlConfg da Windows 7, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ad80f-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="ad80f-116">Aggiornare tutti gli script che chiamano pkgmgr, PEImg o IntlConfg per chiamare gestione e manutenzione immagini distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ad80f-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="ad80f-117">È importante includere l'aggiornamento degli script pkgmgr in questo sforzo, perché lo shim che fornisce la compatibilità con le versioni precedenti di pkgmgr verrà rimosso nelle versioni future dei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="ad80f-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="ad80f-118">Verificare che le chiamate a DISM abbiano sostituito le chiamate a pkgmgr, PEImg e IntlConfg e che l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ad80f-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad80f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad80f-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad80f-120">[Gestione e manutenzione immagini distribuzione (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ad80f-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
