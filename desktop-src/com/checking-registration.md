---
title: Verifica della registrazione
description: Verifica della registrazione
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955285"
---
# <a name="checking-registration"></a><span data-ttu-id="65fbe-103">Verifica della registrazione</span><span class="sxs-lookup"><span data-stu-id="65fbe-103">Checking Registration</span></span>

<span data-ttu-id="65fbe-104">Ogni volta che un'applicazione viene caricata, deve controllare la registrazione per determinare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="65fbe-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="65fbe-105">Indica se i CLSID sono presenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="65fbe-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="65fbe-106">Se non sono presenti, l'applicazione deve registrarsi come installazione originale.</span><span class="sxs-lookup"><span data-stu-id="65fbe-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="65fbe-107">Indica se i CLSID dell'applicazione sono presenti nel registro ma non contengono informazioni correlate a OLE 2.</span><span class="sxs-lookup"><span data-stu-id="65fbe-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="65fbe-108">In tal caso, l'applicazione deve registrarsi come installazione originale.</span><span class="sxs-lookup"><span data-stu-id="65fbe-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="65fbe-109">Indica se il percorso contenente le voci del server ([LocalServer](localserver.md) e [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) punta alla posizione in cui è attualmente installata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="65fbe-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="65fbe-110">Se il percorso non è, riscrivere le voci del percorso in modo che puntino alla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="65fbe-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65fbe-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65fbe-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65fbe-112">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="65fbe-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




