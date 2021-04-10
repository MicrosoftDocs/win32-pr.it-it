---
title: Gestione animazioni Windows
description: Gestione animazioni Windows (animazione Windows) consente un'animazione avanzata degli elementi dell'interfaccia utente.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animazione Windows animazione Windows, portale
- Animazione Windows di gestione animazioni Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963205"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="73db0-105">Gestione animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="73db0-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="73db0-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="73db0-106">Purpose</span></span>

<span data-ttu-id="73db0-107">Gestione animazioni Windows (animazione Windows) consente un'animazione avanzata degli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="73db0-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="73db0-108">È progettato per semplificare il processo di aggiunta dell'animazione all'interfaccia utente di un'applicazione e per consentire agli sviluppatori di implementare animazioni uniformi, naturali e interattive.</span><span class="sxs-lookup"><span data-stu-id="73db0-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="73db0-109">Il Framework di animazione gestisce la pianificazione e l'esecuzione di animazioni.</span><span class="sxs-lookup"><span data-stu-id="73db0-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="73db0-110">Fornisce una libreria di funzioni matematiche utili per specificare il comportamento di un elemento dell'interfaccia utente nel tempo e consente inoltre agli sviluppatori di implementare funzioni personalizzate che forniscono comportamenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="73db0-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="73db0-111">L'animazione Windows non esegue il rendering. può essere usato con qualsiasi piattaforma grafica, tra cui Direct2D, Direct3D o GDI+.</span><span class="sxs-lookup"><span data-stu-id="73db0-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="73db0-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="73db0-112">In this section</span></span>



| <span data-ttu-id="73db0-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="73db0-113">Topic</span></span>                                                                                   | <span data-ttu-id="73db0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73db0-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73db0-115">Guida allo sviluppo di animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="73db0-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="73db0-116">Nella Guida per gli sviluppatori viene fornita una panoramica dell'animazione di Windows e viene fornito codice di esempio che illustra le attività di animazione di base.</span><span class="sxs-lookup"><span data-stu-id="73db0-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="73db0-117">Informazioni di riferimento sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="73db0-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="73db0-118">Negli argomenti contenuti in questa sezione vengono fornite le specifiche di riferimento per gestione animazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="73db0-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="73db0-119">Esempi di animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="73db0-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="73db0-120">Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager.</span><span class="sxs-lookup"><span data-stu-id="73db0-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="73db0-121">Glossario animazione Windows</span><span class="sxs-lookup"><span data-stu-id="73db0-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="73db0-122">Questo glossario contiene i termini e gli acronimi di interesse per gli sviluppatori che utilizzano Windows Animation Manager.</span><span class="sxs-lookup"><span data-stu-id="73db0-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="73db0-123">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="73db0-123">Developer audience</span></span>

<span data-ttu-id="73db0-124">L'animazione Windows è progettata per l'uso da parte di sviluppatori C/C++ esperti che hanno familiarità con i concetti COM, di programmazione dell'interfaccia utente e i concetti di animazione generale.</span><span class="sxs-lookup"><span data-stu-id="73db0-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="73db0-125">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="73db0-125">Run-time requirements</span></span>

<span data-ttu-id="73db0-126">Windows Animation Manager è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73db0-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="73db0-127">Le applicazioni che richiedono il supporto per Windows Animation Manager in Windows Vista possono utilizzare l'aggiornamento della piattaforma per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="73db0-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="73db0-128">Le applicazioni che richiedono l'aggiornamento della piattaforma per Windows Vista possono avere Windows Update verificare che sia installato o scaricarlo e installarlo in background in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="73db0-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="73db0-129">Per ulteriori informazioni, vedere [informazioni sull'aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73db0-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73db0-130">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="73db0-130">Additional resources</span></span>

-   <span data-ttu-id="73db0-131">[Cenni preliminari sull'animazione Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span><span class="sxs-lookup"><span data-stu-id="73db0-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="73db0-132">[All'interno di Windows 7: Deep Dive and tutorial di Animation Manager](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span><span class="sxs-lookup"><span data-stu-id="73db0-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="73db0-133">[Animazione Windows-argomenti avanzati](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span><span class="sxs-lookup"><span data-stu-id="73db0-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="73db0-134">Codice di esempio di Windows Animation Manager</span><span class="sxs-lookup"><span data-stu-id="73db0-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="73db0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73db0-135">Related topics</span></span>

[<span data-ttu-id="73db0-136">Cenni preliminari sull'animazione (.NET Framework)</span><span class="sxs-lookup"><span data-stu-id="73db0-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)