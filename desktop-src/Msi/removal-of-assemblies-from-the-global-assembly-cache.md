---
description: Il Windows Installer determina se consentire la rimozione di un assembly Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Rimozione di assembly dalla Global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231537"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="77e09-103">Rimozione di assembly dalla Global assembly cache</span><span class="sxs-lookup"><span data-stu-id="77e09-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="77e09-104">Il Windows Installer determina se consentire la rimozione di un assembly Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly.</span><span class="sxs-lookup"><span data-stu-id="77e09-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="77e09-105">Il Windows Installer mantiene un bit pin per rappresentare Windows Installer client dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="77e09-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="77e09-106">Il programma di installazione aggiunge l'assembly per il primo client di Windows Installer e lo sblocca quando viene rimosso l'ultimo client Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="77e09-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="77e09-107">L'assembly gestisce un bit pin per ogni client di un assembly.</span><span class="sxs-lookup"><span data-stu-id="77e09-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="77e09-108">Il Windows Installer non è responsabile direttamente della rimozione fisica di Common Language Runtime assembly dal computer.</span><span class="sxs-lookup"><span data-stu-id="77e09-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="77e09-109">Il programma di installazione Sblocca l'assembly quando viene rimosso l'ultimo client di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="77e09-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="77e09-110">Se il Windows Installer è l'ultimo client dell'assembly, il Common Language Runtime fornisce l'opzione per forzare una pulizia sincrona dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="77e09-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="77e09-111">Il processo di pulizia è atomico e non è presente alcun provisioning per un "rollback" a questo punto.</span><span class="sxs-lookup"><span data-stu-id="77e09-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="77e09-112">Quando l'utente ha avuto la possibilità di annullare l'installazione o la rimozione, tutti gli assembly di Common Language Runtime devono essere rilevati.</span><span class="sxs-lookup"><span data-stu-id="77e09-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



