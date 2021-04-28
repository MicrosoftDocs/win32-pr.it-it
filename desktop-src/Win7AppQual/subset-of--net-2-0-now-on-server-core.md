---
description: Subset di .NET 2.0 ora in Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subset di .NET 2.0 ora in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116149"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="f80e5-103">Subset di .NET 2.0 ora in Server Core</span><span class="sxs-lookup"><span data-stu-id="f80e5-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="f80e5-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="f80e5-104">Platform</span></span>

<span data-ttu-id="f80e5-105">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f80e5-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="f80e5-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="f80e5-106">Feature Impact</span></span>

 <span data-ttu-id="f80e5-107">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="f80e5-107">**Severity** - Low</span></span>  
<span data-ttu-id="f80e5-108">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="f80e5-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="f80e5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f80e5-109">Description</span></span>

<span data-ttu-id="f80e5-110">L'opzione di installazione Dei componenti di base del server per Windows Server 2008 R2 include ora un subset .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="f80e5-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="f80e5-111">Il subset è la funzionalità di .NET 2.0 allineata alla funzionalità in Server Core. Non sono stati aggiunti file binari alla base di Server Core per consentire il funzionamento di qualsiasi parte di .NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="f80e5-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="f80e5-112">L'opzione di installazione Dei componenti di base del server per Windows Server 2008 non supporta .NET.</span><span class="sxs-lookup"><span data-stu-id="f80e5-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f80e5-113">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="f80e5-113">Manifestation of Impact</span></span>

<span data-ttu-id="f80e5-114">In questo modo alcune applicazioni basate su .NET 2.0 possono essere eseguite in Server Core in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f80e5-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="f80e5-115">Test</span><span class="sxs-lookup"><span data-stu-id="f80e5-115">Testing</span></span>

<span data-ttu-id="f80e5-116">Verificare che le classi .NET utilizzate dal codice siano incluse in Server Core.</span><span class="sxs-lookup"><span data-stu-id="f80e5-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="f80e5-117">Testare anche tutte le applicazioni che eseguono questo codice in Server Core.</span><span class="sxs-lookup"><span data-stu-id="f80e5-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f80e5-118">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="f80e5-118">Links to Other Resources</span></span>

-   <span data-ttu-id="f80e5-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f80e5-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="f80e5-120">Blog dei componenti di base del server</span><span class="sxs-lookup"><span data-stu-id="f80e5-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="f80e5-121">*Vedere anche* la sezione Server Core di *Windows Server 2008 R2 SDK* quando diventa disponibile</span><span class="sxs-lookup"><span data-stu-id="f80e5-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="f80e5-122">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="f80e5-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
