---
title: Riferimento al modello a oggetti di Windows Media Player
description: Riferimento al modello a oggetti di Windows Media Player
ms.assetid: af313b94-230b-47d7-a3ad-7e23b669886f
keywords:
- Windows Media Player, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- Modello a oggetti di Windows Media Player, riferimento
- modello a oggetti, riferimento
- Controllo ActiveX, riferimento
- Controllo ActiveX di Windows Media Player, riferimento
- Controllo ActiveX Windows Media Player Mobile, riferimento
- informazioni di riferimento sul modello a oggetti, about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6128ff3f69968ddf4f8a35955907a18876ef090
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045238"
---
# <a name="windows-media-player-object-model-reference"></a><span data-ttu-id="4114c-111">Riferimento al modello a oggetti di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="4114c-111">Windows Media Player Object Model Reference</span></span>

<span data-ttu-id="4114c-112">Le sezioni di riferimento del modello a oggetti di Windows Media Player contengono informazioni dettagliate sul modello a oggetti del controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4114c-112">The Windows Media Player Object Model Reference sections contain detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="4114c-113">Il modello a oggetti fornisce interfacce che consentono agli sviluppatori di aggiungere funzionalità di Windows Media Player a pagine Web, programmi C++ e applicazioni .NET.</span><span class="sxs-lookup"><span data-stu-id="4114c-113">The object model provides interfaces that let developers add Windows Media Player functionality to webpages, C++ programs, and .NET applications.</span></span>

<span data-ttu-id="4114c-114">Il riferimento del modello a oggetti per lo scripting viene presentato in uno stile progettato per essere utilizzato con linguaggi di script come Microsoft JScript e documenta il modello a oggetti in termini di oggetti con proprietà, metodi ed eventi associati.</span><span class="sxs-lookup"><span data-stu-id="4114c-114">The Object Model Reference for Scripting is presented in a style designed for use with script languages like Microsoft JScript, and it documents the object model in terms of objects with their associated properties, methods, and events.</span></span>

<span data-ttu-id="4114c-115">Il riferimento del modello a oggetti per C++ fornisce la documentazione per le interfacce COM che i programmatori C++ possono usare per comunicare con il controllo ActiveX di Windows Media Player o il controllo ActiveX Windows Media Player mobile.</span><span class="sxs-lookup"><span data-stu-id="4114c-115">The Object Model Reference for C++ provides documentation for COM interfaces that C++ programmers can use to communicate with the Windows Media Player ActiveX control or the Windows Media Player Mobile ActiveX control.</span></span> <span data-ttu-id="4114c-116">La maggior parte di queste interfacce viene implementata dal controllo Media Player di Windows e viene chiamata dall'applicazione C++.</span><span class="sxs-lookup"><span data-stu-id="4114c-116">Most of these interfaces are implemented by Windows Media Player control and called by the C++ application.</span></span> <span data-ttu-id="4114c-117">Tuttavia, alcune interfacce, ad esempio **IWMPEvents** e **IWMPRemoteMediaServices**, vengono implementate dall'applicazione C++ e chiamate dal controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="4114c-117">However, some of the interfaces (for example, **IWMPEvents** and **IWMPRemoteMediaServices**) are implemented by the C++ application and called by the Windows Media Player control.</span></span>

<span data-ttu-id="4114c-118">Il riferimento del modello a oggetti per Visual Basic .NET e C# fornisce la documentazione per le proprietà, i metodi e gli eventi dell'oggetto **AxWindowsMediaPlayer** e per le interfacce del controllo ActiveX di Windows Media Player disponibili tramite l'interoperabilità COM in una soluzione codificata in Visual Studio .NET 2002 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4114c-118">The Object Model Reference for Visual Basic .NET and C# provides documentation for the properties, methods, and events of the **AxWindowsMediaPlayer** object and for interfaces to the Windows Media Player ActiveX control that are available through COM interoperability in a solution coded in Visual Studio .NET 2002 or later.</span></span>

<span data-ttu-id="4114c-119">Il riferimento del modello a oggetti di Windows Media Player contiene le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="4114c-119">The Windows Media Player Object Model Reference contains the following sections.</span></span>



| <span data-ttu-id="4114c-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="4114c-120">Section</span></span>                                                                                                        | <span data-ttu-id="4114c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4114c-121">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4114c-122">Riferimento del modello a oggetti per lo scripting</span><span class="sxs-lookup"><span data-stu-id="4114c-122">Object Model Reference for Scripting</span></span>](object-model-reference-for-scripting.md)                               | <span data-ttu-id="4114c-123">Fornisce la documentazione di riferimento per le proprietà, i metodi e gli eventi resi disponibili dal modello a oggetti per i linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="4114c-123">Provides reference documentation for the properties, methods, and events that the object model makes available to scripting languages.</span></span> <span data-ttu-id="4114c-124">Queste informazioni sono utili anche per la programmazione Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="4114c-124">This information is also useful for Visual Basic 6.0 programming.</span></span> |
| [<span data-ttu-id="4114c-125">Riferimento del modello a oggetti per C++</span><span class="sxs-lookup"><span data-stu-id="4114c-125">Object Model Reference for C++</span></span>](object-model-reference-for-c.md)                                             | <span data-ttu-id="4114c-126">Fornisce la documentazione di riferimento per le interfacce C++.</span><span class="sxs-lookup"><span data-stu-id="4114c-126">Provides reference documentation for C++ interfaces.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="4114c-127">Riferimento del modello a oggetti per Visual Basic .NET e C #</span><span class="sxs-lookup"><span data-stu-id="4114c-127">Object Model Reference for Visual Basic .NET and C#</span></span>](object-model-reference-for-visual-basic--net-and-c.md) | <span data-ttu-id="4114c-128">Fornisce la documentazione di riferimento per gli oggetti e le interfacce disponibili per Visual Basic programmatori .NET e C# tramite l'interoperabilità COM.</span><span class="sxs-lookup"><span data-stu-id="4114c-128">Provides reference documentation for objects and interfaces available to Visual Basic .NET and C# programmers through COM interoperability.</span></span>                                                             |
| [<span data-ttu-id="4114c-129">Riferimento agli attributi</span><span class="sxs-lookup"><span data-stu-id="4114c-129">Attribute Reference</span></span>](attribute-reference.md)                                                                 | <span data-ttu-id="4114c-130">Fornisce la documentazione di riferimento per gli attributi di metadati di interesse per gli sviluppatori di Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="4114c-130">Provides reference documentation for metadata attributes that are of interest to Windows Media Player SDK developers.</span></span>                                                                                    |
| [<span data-ttu-id="4114c-131">Tipi di enumerazione</span><span class="sxs-lookup"><span data-stu-id="4114c-131">Enumeration Types</span></span>](enumeration-types.md)                                                                     | <span data-ttu-id="4114c-132">Fornisce la documentazione di riferimento per i tipi di enumerazione utilizzati dalle interfacce C++ e .NET.</span><span class="sxs-lookup"><span data-stu-id="4114c-132">Provides reference documentation for the enumeration types that are used by the C++ and .NET interfaces.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="4114c-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4114c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4114c-134">**Modello a oggetti di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="4114c-134">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




