---
title: Microsoft Active Accessibility
description: Microsoft Active Accessibility è una tecnologia basata su Component Object Model (COM) che migliora il modo in cui gli strumenti di accessibilità funzionano con le applicazioni eseguite in Microsoft Windows.
ms.assetid: f3e31c6f-c49e-4a61-99f1-b695ece2bfc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef277e54c34b64747811c4db40ecfb8fa1fb6bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728770"
---
# <a name="microsoft-active-accessibility"></a><span data-ttu-id="631eb-103">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="631eb-103">Microsoft Active Accessibility</span></span>

## <a name="purpose"></a><span data-ttu-id="631eb-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="631eb-104">Purpose</span></span>

<span data-ttu-id="631eb-105">Microsoft Active Accessibility è una tecnologia basata su Component Object Model (COM) che migliora il modo in cui gli strumenti di accessibilità funzionano con le applicazioni eseguite in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="631eb-105">Microsoft Active Accessibility is a Component Object Model (COM)-based technology that improves the way accessibility aids work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="631eb-106">Fornisce librerie a collegamento dinamico incorporate nel sistema operativo, nonché un'interfaccia COM e elementi API che forniscono metodi affidabili per esporre le informazioni sugli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="631eb-106">It provides dynamic-link libraries that are incorporated into the operating system as well as a COM interface and API elements that provide reliable methods for exposing information about UI elements.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="631eb-107">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="631eb-107">Where applicable</span></span>

<span data-ttu-id="631eb-108">Utilizzando Microsoft Active Accessibility e le seguenti procedure di progettazione accessibili, gli sviluppatori possono rendere le applicazioni in esecuzione in Windows più accessibili a molti utenti con esigenze di visione, udito o movimento.</span><span class="sxs-lookup"><span data-stu-id="631eb-108">By using Microsoft Active Accessibility and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="631eb-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="631eb-109">Developer audience</span></span>

<span data-ttu-id="631eb-110">Microsoft Active Accessibility è progettato principalmente per gli sviluppatori C, C++ e Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="631eb-110">Microsoft Active Accessibility is designed primarily for C, C++, and Microsoft Visual Basic developers.</span></span> <span data-ttu-id="631eb-111">In generale, gli sviluppatori necessitano di un livello moderato di informazioni sugli oggetti COM e sulle interfacce, oltre che su Unicode.</span><span class="sxs-lookup"><span data-stu-id="631eb-111">In general, developers need a moderate level of understanding about COM objects and interfaces as well as about Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="631eb-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="631eb-112">Run-time requirements</span></span>

<span data-ttu-id="631eb-113">Il supporto completo per Microsoft Active Accessibility è integrato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="631eb-113">Full support for Microsoft Active Accessibility is built into Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="631eb-114">Microsoft Active Accessibility è inoltre supportato in Windows NT 4,0 con Service Pack 6 (SP6) e versioni successive e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="631eb-114">Microsoft Active Accessibility is also supported on Windows NT 4.0 with Service Pack 6 (SP6) and later, and Windows 98.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="631eb-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="631eb-115">In this section</span></span>



| <span data-ttu-id="631eb-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="631eb-116">Topic</span></span>                                                             | <span data-ttu-id="631eb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="631eb-117">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="631eb-118">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="631eb-118">Getting Started</span></span>](getting-started.md)<br/>                 | <span data-ttu-id="631eb-119">Introduzione ai componenti di Microsoft Active Accessibility e alle piattaforme supportate e a un breve confronto tra Microsoft Active Accessibility e automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="631eb-119">Introduction to the Microsoft Active Accessibility components and the supported platforms, and a brief comparison of Microsoft Active Accessibility and Microsoft UI Automation.</span></span><br/> |
| [<span data-ttu-id="631eb-120">Panoramica tecnica</span><span class="sxs-lookup"><span data-stu-id="631eb-120">Technical Overview</span></span>](technical-overview.md)<br/>           | <span data-ttu-id="631eb-121">Informazioni generali sulla tecnologia Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="631eb-121">General information about Microsoft Active Accessibility technology.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="631eb-122">Guida per gli sviluppatori in C/C++</span><span class="sxs-lookup"><span data-stu-id="631eb-122">C/C++ Developer's Guide</span></span>](c-c---developer-s-guide.md)<br/> | <span data-ttu-id="631eb-123">Informazioni sul funzionamento di Microsoft Active Accessibility dal punto di vista di uno sviluppatore di applicazioni C o C++.</span><span class="sxs-lookup"><span data-stu-id="631eb-123">Information about how Microsoft Active Accessibility works from the perspective of a C or C++ application developer.</span></span> <span data-ttu-id="631eb-124">Vengono illustrati i problemi specifici degli sviluppatori client e server.</span><span class="sxs-lookup"><span data-stu-id="631eb-124">It covers issues specific to client and server developers.</span></span><br/>  |
| [<span data-ttu-id="631eb-125">Riferimenti per C/C++</span><span class="sxs-lookup"><span data-stu-id="631eb-125">C/C++ Reference</span></span>](c-c---reference.md)<br/>                 | <span data-ttu-id="631eb-126">Documentazione di riferimento sull'API di Microsoft Active Accessibility per gli sviluppatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="631eb-126">Reference documentation about the Microsoft Active Accessibility API for C/C++ developers.</span></span><br/>                                                                                       |
| [<span data-ttu-id="631eb-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="631eb-127">Samples</span></span>](samples.md)<br/>                                 | <span data-ttu-id="631eb-128">Programmi di esempio che illustrano come usare l'API di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="631eb-128">Sample programs that demonstrate how to use the Microsoft Active Accessibility API.</span></span><br/>                                                                                              |
| [<span data-ttu-id="631eb-129">Appendici</span><span class="sxs-lookup"><span data-stu-id="631eb-129">Appendixes</span></span>](appendixes.md)<br/>                           | <span data-ttu-id="631eb-130">Materiale di riferimento aggiuntivo per sviluppatori Microsoft Active Accessibility client e server e Visual Basic sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="631eb-130">Additional reference material for Microsoft Active Accessibility client and server developers and Visual Basic developers.</span></span><br/>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="631eb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="631eb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="631eb-132">sito Web Microsoft dedicato all'accessibilità</span><span class="sxs-lookup"><span data-stu-id="631eb-132">Microsoft Accessibility website</span></span>](https://www.microsoft.com/enable/)
</dt> <dt>

[<span data-ttu-id="631eb-133">Microsoft Accessibility Developer Center su MSDN</span><span class="sxs-lookup"><span data-stu-id="631eb-133">Microsoft Accessibility Developer Center on MSDN</span></span>](/windows/apps/accessibility)
</dt> </dl>

 

