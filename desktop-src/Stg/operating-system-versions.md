---
title: Versioni del sistema operativo
description: Questo tipo di dati DWORD deve avere il tipo di sistema operativo nella parola più ordinata e il numero di versione del sistema operativo nella parola di basso livello. Nella tabella seguente sono elencati i valori possibili per il sistema operativo.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Archiviazione strutturata versioni del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299986"
---
# <a name="operating-system-versions"></a><span data-ttu-id="216c9-105">Versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="216c9-105">Operating System Versions</span></span>

<span data-ttu-id="216c9-106">Questo tipo di dati **DWORD** deve avere il tipo di sistema operativo nella parola più ordinata e il numero di versione del sistema operativo nella parola di basso livello.</span><span class="sxs-lookup"><span data-stu-id="216c9-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="216c9-107">Nella tabella seguente sono elencati i valori possibili per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="216c9-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="216c9-108">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="216c9-108">Operating system</span></span>       | <span data-ttu-id="216c9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="216c9-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="216c9-110">Windows a 32 bit (Win32)</span><span class="sxs-lookup"><span data-stu-id="216c9-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="216c9-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="216c9-111">0x0002</span></span> |
| <span data-ttu-id="216c9-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="216c9-112">Macintosh</span></span>              | <span data-ttu-id="216c9-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="216c9-113">0x0001</span></span> |
| <span data-ttu-id="216c9-114">Windows a 16 bit (Win16)</span><span class="sxs-lookup"><span data-stu-id="216c9-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="216c9-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="216c9-115">0x0000</span></span> |



 

<span data-ttu-id="216c9-116">Per i sistemi operativi Microsoft Windows, la versione del sistema operativo è la parola di ordine inferiore restituita dalla funzione [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) .</span><span class="sxs-lookup"><span data-stu-id="216c9-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="216c9-117">Per Microsoft Windows, il codice di esempio seguente imposta correttamente la versione del sistema operativo di origine.</span><span class="sxs-lookup"><span data-stu-id="216c9-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 