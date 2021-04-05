---
title: Il sistema operativo ora controlla l'alimentazione alle unità disco ottico
description: Il sistema operativo ora controlla l'alimentazione alle unità disco ottico
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730735"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="98728-103">Il sistema operativo ora controlla l'alimentazione alle unità disco ottico</span><span class="sxs-lookup"><span data-stu-id="98728-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="98728-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="98728-104">Platforms</span></span>

<span data-ttu-id="98728-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="98728-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="98728-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98728-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="98728-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98728-107">Description</span></span>

<span data-ttu-id="98728-108">Nelle versioni precedenti di Windows, l'alimentazione dell'unità ottica non è stata gestita quando l'unità ottica non è in uso.</span><span class="sxs-lookup"><span data-stu-id="98728-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="98728-109">A questo punto, se non è presente alcun supporto nell'unità disco ottico (dispari), il sistema operativo disattiva l'alimentazione dell'unità ottica.</span><span class="sxs-lookup"><span data-stu-id="98728-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="98728-110">Questa funzionalità è denominata zero Power ODD (ZPODD).</span><span class="sxs-lookup"><span data-stu-id="98728-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="98728-111">Questa funzionalità è applicabile solo alle unità ottiche che usano un connettore SATA (Serial Advanced Technology Attachment).</span><span class="sxs-lookup"><span data-stu-id="98728-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="98728-112">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="98728-112">Manifestation</span></span>

<span data-ttu-id="98728-113">Non sono stati rilevati effetti negativi da questo nuovo comportamento. è tuttavia necessario tenerne conto perché potrebbe causare un comportamento imprevisto del software per la scrittura di contenuti multimediali.</span><span class="sxs-lookup"><span data-stu-id="98728-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="98728-114">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="98728-114">Mitigation</span></span>

<span data-ttu-id="98728-115">Per ripristinare lo stato always on, disattivare questa funzionalità nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="98728-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="98728-116">Il percorso assoluto del valore del registro di sistema è:</span><span class="sxs-lookup"><span data-stu-id="98728-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="98728-117">Il tipo è DWORD (32 bit) e se il valore è 0, ZPODD è disabilitato; Se è qualsiasi altro valore, ZPODD è abilitato.</span><span class="sxs-lookup"><span data-stu-id="98728-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="98728-118">Test</span><span class="sxs-lookup"><span data-stu-id="98728-118">Tests</span></span>

<span data-ttu-id="98728-119">Testare il software per la scrittura di contenuti multimediali per eventuali anomalie che si verificano a causa di questa nuova funzionalità.</span><span class="sxs-lookup"><span data-stu-id="98728-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="98728-120">[Segnala a Microsoft](mailto:OptIssue@microsoft.com) eventuali problemi riscontrati con questa nuova funzionalità.</span><span class="sxs-lookup"><span data-stu-id="98728-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




