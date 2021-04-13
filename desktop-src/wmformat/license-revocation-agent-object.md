---
title: Oggetto agente di revoca licenze
description: Oggetto agente di revoca licenze
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK, oggetti dell'agente di revoca delle licenze
- ASF (Advanced Systems Format), oggetti dell'agente di revoca delle licenze
- ASF (formato avanzato dei sistemi), oggetti dell'agente di revoca delle licenze
- oggetti, oggetti dell'agente di revoca delle licenze
- revoca delle licenze, oggetti dell'agente di revoca delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398548"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="abe3d-108">Oggetto agente di revoca licenze</span><span class="sxs-lookup"><span data-stu-id="abe3d-108">License Revocation Agent Object</span></span>

<span data-ttu-id="abe3d-109">L'oggetto agente di revoca licenze gestisce il lato client della revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="abe3d-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="abe3d-110">La revoca delle licenze è il processo mediante il quale un server licenze può rimuovere le licenze dall'archivio licenze nel computer client.</span><span class="sxs-lookup"><span data-stu-id="abe3d-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="abe3d-111">Il processo implica il passaggio di diversi messaggi tra l'applicazione client e il server licenze.</span><span class="sxs-lookup"><span data-stu-id="abe3d-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="abe3d-112">I metodi esposti in questo oggetto elaborano e generano tali messaggi.</span><span class="sxs-lookup"><span data-stu-id="abe3d-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="abe3d-113">L'oggetto dell'agente di revoca delle licenze viene creato dalla funzione [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , che imposta un puntatore a un'interfaccia [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="abe3d-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="abe3d-114">**IUnknown** e **IWMLicenseRevocationAgent** sono le uniche interfacce supportate da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="abe3d-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abe3d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abe3d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe3d-116">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="abe3d-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




