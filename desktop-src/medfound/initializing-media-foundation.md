---
description: Inizializzazione di Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inizializzazione di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320753"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="3fac3-103">Inizializzazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3fac3-103">Initializing Media Foundation</span></span>

<span data-ttu-id="3fac3-104">Prima di usare oggetti o interfacce di Microsoft Media Foundation, è necessario chiamare la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="3fac3-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="3fac3-105">Passare la costante **MF \_ Version**.</span><span class="sxs-lookup"><span data-stu-id="3fac3-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="3fac3-106">La funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Inizializza la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3fac3-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="3fac3-107">Se **MFStartup** restituisce la \_ versione MF E \_ Bad \_ Startup \_ , significa che l'applicazione è stata compilata utilizzando una versione delle intestazioni Media Foundation che non corrispondono alle dll Media Foundation nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3fac3-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="3fac3-108">Per ogni chiamata a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), l'applicazione deve chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="3fac3-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="3fac3-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fac3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fac3-110">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3fac3-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="3fac3-111">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3fac3-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



