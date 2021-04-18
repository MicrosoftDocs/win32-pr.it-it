---
title: Il modello presente in coda verrà deprecato
description: Il modello presente in coda verrà deprecato
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300634"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="01f34-103">Il modello presente in coda verrà deprecato</span><span class="sxs-lookup"><span data-stu-id="01f34-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="01f34-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="01f34-104">Platforms</span></span>

<span data-ttu-id="01f34-105">**Client** -dopo Windows 8</span><span class="sxs-lookup"><span data-stu-id="01f34-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="01f34-106">**Server** : dopo Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01f34-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="01f34-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01f34-107">Description</span></span>

<span data-ttu-id="01f34-108">Nella versione di Windows dopo Windows 8, queste API restituiranno E \_ NOTIMPL:</span><span class="sxs-lookup"><span data-stu-id="01f34-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="01f34-109">DwmSetPresentParameters</span><span class="sxs-lookup"><span data-stu-id="01f34-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="01f34-110">DwmSetDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="01f34-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="01f34-111">DwmModifyPreviousDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="01f34-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="01f34-112">Inoltre, questa API accetterà solo il valore NULL per il parametro HWND:</span><span class="sxs-lookup"><span data-stu-id="01f34-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="01f34-113">DwmGetCompositionTimingInfo</span><span class="sxs-lookup"><span data-stu-id="01f34-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="01f34-114">Si interromperà il supporto di DwmGetCompositionTimingInfo con HWND! = NULL e si rimuove la funzionalità associata.</span><span class="sxs-lookup"><span data-stu-id="01f34-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="01f34-115">Se viene specificato un valore non NULL per HWND, l'API restituirà E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="01f34-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="01f34-116">Viene anche sconsigliato l'uso dell'API DwmGetCompositionTimingInfo e si suggerisce agli sviluppatori di passare al modello DXGI Flip e alle API di DX present associate.</span><span class="sxs-lookup"><span data-stu-id="01f34-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="01f34-117">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="01f34-117">Manifestation</span></span>

<span data-ttu-id="01f34-118">Le applicazioni che utilizzano il modello presente in coda non funzioneranno correttamente.</span><span class="sxs-lookup"><span data-stu-id="01f34-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="01f34-119">La manifestazione esatta dipende dall'applicazione specifica, ma può variare da un intervallo di presentazione non corretto all'uscita dall'applicazione in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="01f34-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="01f34-120">In pratica, non ci si aspetta di vedere molte applicazioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="01f34-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="01f34-121">Questo modello è stato usato da Vista Media Player, che non verrà usato in Windows 8 (e possibilmente con il lettore Zune precedente).</span><span class="sxs-lookup"><span data-stu-id="01f34-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="01f34-122">Al momento non sono disponibili informazioni su altre applicazioni che utilizzano effettivamente questo modello.</span><span class="sxs-lookup"><span data-stu-id="01f34-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="01f34-123">Soluzione</span><span class="sxs-lookup"><span data-stu-id="01f34-123">Solution</span></span>

<span data-ttu-id="01f34-124">Gli sviluppatori devono usare la modalità DXGI Flip Presentation invece della presente in coda (disponibile nel runtime di DX9 da Windows 7 e nei runtime DX10 e DX11 in Windows 8).</span><span class="sxs-lookup"><span data-stu-id="01f34-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="01f34-125">Test</span><span class="sxs-lookup"><span data-stu-id="01f34-125">Tests</span></span>

<span data-ttu-id="01f34-126">Eseguire test generali per assicurarsi che i componenti Windows della posta in arrivo e i prodotti principali continuino a funzionare alla prossima versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="01f34-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 




