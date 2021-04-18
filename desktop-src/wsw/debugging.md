---
title: Debug (servizi Web Windows)
description: Un set di funzioni è disponibile solo nella build di DEBUG e è destinato a test e debug.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debug di servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300812"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="efebd-106">Debug (servizi Web Windows)</span><span class="sxs-lookup"><span data-stu-id="efebd-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="efebd-107">Un set di funzioni è disponibile solo nella build di DEBUG e è destinato a test e debug.</span><span class="sxs-lookup"><span data-stu-id="efebd-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="efebd-108">Sono disponibili diverse funzioni e variabili di ambiente solo in modalità di DEBUG.</span><span class="sxs-lookup"><span data-stu-id="efebd-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="efebd-109">Possono essere usati per semplificare il test e il debug.</span><span class="sxs-lookup"><span data-stu-id="efebd-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="efebd-110">Se si imposta WsTimeout = 0, tutti i timeout saranno infiniti.</span><span class="sxs-lookup"><span data-stu-id="efebd-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="efebd-111">Questa operazione è utile quando si esegue il debug del debugger durante le operazioni sensibili al tempo.</span><span class="sxs-lookup"><span data-stu-id="efebd-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="efebd-112">L'impostazione di WsFailCount ha lo stesso effetto della chiamata di WsSetAutoFail.</span><span class="sxs-lookup"><span data-stu-id="efebd-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="efebd-113">WsFlags consente di impostare diversi flag che modificano il comportamento in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="efebd-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="efebd-114">La sintassi è WsFlags = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="efebd-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="efebd-115">I flag supportati sono ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest e ModifySignatureValue.</span><span class="sxs-lookup"><span data-stu-id="efebd-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="efebd-116">Con il debug vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="efebd-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="efebd-117">**WsDumpMemory**</span><span class="sxs-lookup"><span data-stu-id="efebd-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="efebd-118">**WsSetAutoFail**</span><span class="sxs-lookup"><span data-stu-id="efebd-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




