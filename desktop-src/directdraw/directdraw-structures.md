---
title: Strutture DirectDraw
description: Questa sezione contiene informazioni sulle strutture seguenti usate con DirectDraw
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300666"
---
# <a name="directdraw-structures"></a><span data-ttu-id="7ae0b-103">Strutture DirectDraw</span><span class="sxs-lookup"><span data-stu-id="7ae0b-103">DirectDraw Structures</span></span>

<span data-ttu-id="7ae0b-104">In questa sezione vengono fornite informazioni sulle seguenti strutture utilizzate con DirectDraw:</span><span class="sxs-lookup"><span data-stu-id="7ae0b-104">This section contains information about the following structures used with DirectDraw:</span></span>

-   [<span data-ttu-id="7ae0b-105">**DDBLTBATCH**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-105">**DDBLTBATCH**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [<span data-ttu-id="7ae0b-106">**DDBLTFX**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-106">**DDBLTFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [<span data-ttu-id="7ae0b-107">**DDCAPS**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-107">**DDCAPS**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [<span data-ttu-id="7ae0b-108">**DDCOLORCONTROL**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-108">**DDCOLORCONTROL**</span></span>](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [<span data-ttu-id="7ae0b-109">**DDCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-109">**DDCOLORKEY**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [<span data-ttu-id="7ae0b-110">**DDDEVICEIDENTIFIER2**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-110">**DDDEVICEIDENTIFIER2**</span></span>](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [<span data-ttu-id="7ae0b-111">**DDGAMMARAMP**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-111">**DDGAMMARAMP**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [<span data-ttu-id="7ae0b-112">**DDOVERLAYFX**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-112">**DDOVERLAYFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [<span data-ttu-id="7ae0b-113">**DDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="7ae0b-113">**DDPIXELFORMAT**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   <span data-ttu-id="7ae0b-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ae0b-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span></span>
-   <span data-ttu-id="7ae0b-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ae0b-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span></span>
-   <span data-ttu-id="7ae0b-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ae0b-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span></span>
-   <span data-ttu-id="7ae0b-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ae0b-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span></span>

> [!Note]  
> <span data-ttu-id="7ae0b-118">Prima di usare la struttura, è necessario inizializzare la memoria per ogni struttura DirectX su 0.</span><span class="sxs-lookup"><span data-stu-id="7ae0b-118">You should initialize the memory for each DirectX structure to 0 before you use the structure.</span></span> <span data-ttu-id="7ae0b-119">Inoltre, per tutte le strutture che contengono un membro **dwSize** , è necessario impostare il membro sulle dimensioni della struttura, in byte, prima che venga utilizzata la struttura.</span><span class="sxs-lookup"><span data-stu-id="7ae0b-119">In addition, for all structures that contain a **dwSize** member, you should set the member to the size of the structure, in bytes, before the structure is used.</span></span> <span data-ttu-id="7ae0b-120">Nell'esempio seguente vengono eseguite queste attività su una struttura comune, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span><span class="sxs-lookup"><span data-stu-id="7ae0b-120">The following example performs these tasks on a common structure, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span></span>

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




