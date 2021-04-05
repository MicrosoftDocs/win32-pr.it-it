---
title: Input MouseWheel per Windows 8.1
description: Input MouseWheel per Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855810"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="bffe9-103">Input MouseWheel per Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bffe9-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="bffe9-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="bffe9-104">Platform</span></span>

<dl> <span data-ttu-id="bffe9-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bffe9-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="bffe9-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bffe9-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="bffe9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bffe9-107">Description</span></span>

<span data-ttu-id="bffe9-108">In Windows 8.1 gli eventi MouseWheel non vengono più recapitati in base allo stato attivo della tastiera come nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="bffe9-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="bffe9-109">In Windows 8.1, se il mouse è posizionato su un'app dello Store, MouseWheel verrà recapitato all'app; per motivi di compatibilità, tuttavia, se il mouse è posizionato su un'applicazione desktop, MouseWheel continuerà a essere recapitato in base allo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="bffe9-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="bffe9-110">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="bffe9-110">Manifestations</span></span>

<span data-ttu-id="bffe9-111">Quando il mouse passa sopra le app dello Store, MouseWheel scorre tutti i contenuti applicabili senza che l'utente debba fare clic sull'app dello Store.</span><span class="sxs-lookup"><span data-stu-id="bffe9-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="bffe9-112">Questo vale anche per la schermata Start.</span><span class="sxs-lookup"><span data-stu-id="bffe9-112">This also applies to the start screen.</span></span> <span data-ttu-id="bffe9-113">Questa operazione rende lo scorrimento di MouseWheel un'interazione più semplice in Windows 8.1 rispetto a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bffe9-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="bffe9-114">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="bffe9-114">Mitigation</span></span>

<span data-ttu-id="bffe9-115">Per la maggior parte, questa modifica non dovrebbe avere alcun effetto sulle app esistenti.</span><span class="sxs-lookup"><span data-stu-id="bffe9-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="bffe9-116">Se un'app dello Store ha ascoltato gli eventi MouseWheel solo dopo aver registrato un evento click del mouse, è probabile che l'app non risponda a MouseWheel fino a quando l'utente non l'ha fatto clic attivamente.</span><span class="sxs-lookup"><span data-stu-id="bffe9-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="bffe9-117">Di conseguenza, l'aspetto più probabile è semplicemente che un'app continui a funzionare esattamente come in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bffe9-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="bffe9-118">Per le app desktop, con lo stato attivo della tastiera non viene più assegnata un'app a Monopoli sull'input di MouseWheel, ma questo non è in alcun modo in grado di interrompere tali app.</span><span class="sxs-lookup"><span data-stu-id="bffe9-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="bffe9-119">Quindi, non è necessaria alcuna mitigazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="bffe9-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="bffe9-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="bffe9-120">Solution</span></span>

<span data-ttu-id="bffe9-121">Gli sviluppatori di app dello Store dovrebbero ricevere eventi MouseWheel senza un evento di clic del mouse precursore.</span><span class="sxs-lookup"><span data-stu-id="bffe9-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="bffe9-122">Non dovrebbero, ad esempio, restare in ascolto di eventi MouseWheel solo dopo la registrazione di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="bffe9-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="bffe9-123">Analogamente, le applicazioni desktop non devono tentare di acquisire gli eventi MouseWheel (ad esempio, impostando un hook di basso livello) quando hanno lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="bffe9-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="bffe9-124">Test</span><span class="sxs-lookup"><span data-stu-id="bffe9-124">Tests</span></span>

<span data-ttu-id="bffe9-125">Gli sviluppatori di App Store devono eseguire test su Windows 8.1 per verificare che tutte le funzionalità di scorrimento funzionino ogni volta che si passa il mouse sull'app.</span><span class="sxs-lookup"><span data-stu-id="bffe9-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="bffe9-126">Gli sviluppatori di app desktop devono eseguire test su Windows 8.1 per verificare che non stiano acquisendo gli eventi MouseWheel (in base alle linee guida indicate in precedenza).</span><span class="sxs-lookup"><span data-stu-id="bffe9-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




