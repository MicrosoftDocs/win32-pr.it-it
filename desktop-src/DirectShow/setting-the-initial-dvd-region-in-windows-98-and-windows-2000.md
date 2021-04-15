---
description: Impostazione dell'area DVD iniziale
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Impostazione dell'area DVD iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520386"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="cde9a-103">Impostazione dell'area DVD iniziale</span><span class="sxs-lookup"><span data-stu-id="cde9a-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="cde9a-104">È responsabilità del produttore del sistema selezionare un'area DVD iniziale per l'unità DVD nei PC.</span><span class="sxs-lookup"><span data-stu-id="cde9a-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="cde9a-105">Per impostare l'area è possibile utilizzare solo dischi crittografati.</span><span class="sxs-lookup"><span data-stu-id="cde9a-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="cde9a-106">Windows 2000 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="cde9a-106">Windows 2000 and Later</span></span>

<span data-ttu-id="cde9a-107">A partire da Windows 2000, l'area DVD predefinita viene selezionata in base alle impostazioni locali per cui è configurato il computer.</span><span class="sxs-lookup"><span data-stu-id="cde9a-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="cde9a-108">Windows 2000 imposta sempre l'area iniziale per un'unità DVD che usa questa area predefinita e l'area del disco, se è presente un disco nell'unità.</span><span class="sxs-lookup"><span data-stu-id="cde9a-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="cde9a-109">Il produttore del sistema non deve eseguire alcuna operazione per impostare l'area iniziale per le unità DVD di Windows 2000 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cde9a-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="cde9a-110">Per le unità RPC1, se non è presente alcun disco nell'unità durante l'avvio, l'area predefinita viene impostata solo in base alle impostazioni locali del computer.</span><span class="sxs-lookup"><span data-stu-id="cde9a-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="cde9a-111">Se è presente un disco DVD nell'unità durante l'avvio, l'area predefinita viene selezionata come area dell'unità, purché corrisponda a un'area del disco; in caso contrario, viene selezionata l'area minima del disco come area iniziale dell'unità.</span><span class="sxs-lookup"><span data-stu-id="cde9a-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="cde9a-112">All'utente (o produttore del sistema) è consentita una modifica rimanente, nel caso in cui il valore predefinito non sia corretto.</span><span class="sxs-lookup"><span data-stu-id="cde9a-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="cde9a-113">Per le unità RPC2, se durante il processo di installazione Windows 2000 rileva che nell'unità non è impostata alcuna area, tenterà di selezionare un'area come sopra, ma solo se è presente un disco nell'unità.</span><span class="sxs-lookup"><span data-stu-id="cde9a-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="cde9a-114">(Le unità RPC1 scelgono l'area senza disco nell'unità).</span><span class="sxs-lookup"><span data-stu-id="cde9a-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="cde9a-115">Una volta impostata un'area per le unità RPC2, non viene modificata automaticamente da una nuova installazione o da un'installazione pulita del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cde9a-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="cde9a-116">L'OEM può impostare una chiave del registro di sistema contenente l'area DVD predefinita per il sistema.</span><span class="sxs-lookup"><span data-stu-id="cde9a-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="cde9a-117">Al primo avvio, l'area dell'unità verrà impostata su questo valore.</span><span class="sxs-lookup"><span data-stu-id="cde9a-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="cde9a-118">La chiave del registro di sistema in Windows 2000 e versioni successive è HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).</span><span class="sxs-lookup"><span data-stu-id="cde9a-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="cde9a-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cde9a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cde9a-120">Supporto delle modifiche all'area DVD in Windows</span><span class="sxs-lookup"><span data-stu-id="cde9a-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



