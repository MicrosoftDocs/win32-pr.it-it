---
description: "Sono disponibili quattro livelli per la libreria di analisi dell'input penna: Windows Form, WPF, COM e il livello di base. In questa sezione viene descritto quando utilizzare ogni livello."
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Utilizzo API analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966515"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="4b4f9-104">Utilizzo API analisi input penna</span><span class="sxs-lookup"><span data-stu-id="4b4f9-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="4b4f9-105">Sono disponibili quattro livelli per la libreria di analisi dell'input penna: Windows Form, WPF, COM e il livello di base.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="4b4f9-106">In questa sezione viene descritto quando utilizzare ogni livello.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="4b4f9-107">Panoramica dell'API di analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4b4f9-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="4b4f9-108">Le librerie di analisi dell'input penna sono progettate per essere usate in un'ampia gamma di ambienti di programmazione supportati.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="4b4f9-109">Sono disponibili quattro livelli di base tramite i quali l'applicazione può usare l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="4b4f9-110">Questi livelli sono:</span><span class="sxs-lookup"><span data-stu-id="4b4f9-110">These layers are:</span></span>

-   <span data-ttu-id="4b4f9-111">Livello Windows Form</span><span class="sxs-lookup"><span data-stu-id="4b4f9-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="4b4f9-112">Livello WPF</span><span class="sxs-lookup"><span data-stu-id="4b4f9-112">The WPF layer</span></span>
-   <span data-ttu-id="4b4f9-113">Livello COM</span><span class="sxs-lookup"><span data-stu-id="4b4f9-113">The COM layer</span></span>
-   <span data-ttu-id="4b4f9-114">Livello di base</span><span class="sxs-lookup"><span data-stu-id="4b4f9-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="4b4f9-115">Applicazioni Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4b4f9-115">Windows Forms Applications</span></span>

<span data-ttu-id="4b4f9-116">È possibile usare l'API di analisi dell'input penna nel progetto gestito aggiungendo un riferimento alle librerie seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b4f9-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="4b4f9-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="4b4f9-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="4b4f9-118">Libreria di analisi documenti input penna (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="4b4f9-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="4b4f9-119">Nelle applicazioni Windows Form è probabile che le librerie vengano utilizzate insieme agli oggetti della piattaforma Tablet PC standard disponibili nell'assembly Microsoft Tablet PC API v 1.7.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="4b4f9-120">Assicurarsi che sia presente anche un riferimento a:</span><span class="sxs-lookup"><span data-stu-id="4b4f9-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="4b4f9-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="4b4f9-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="4b4f9-122">Applicazioni Windows Presentation Framework</span><span class="sxs-lookup"><span data-stu-id="4b4f9-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="4b4f9-123">È possibile usare l'API di analisi dell'input penna nel progetto WPF aggiungendo un riferimento ai membri dell'analisi dell'input penna definiti nello spazio dei nomi System. Windows. Ink nell'assembly IAWinFX.dll.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="4b4f9-124">Questo assembly viene installato dall'SDK.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="4b4f9-125">Applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="4b4f9-125">COM Applications</span></span>

<span data-ttu-id="4b4f9-126">Le applicazioni COM non di automazione devono usare il livello COM delle API di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="4b4f9-127">Tipi di oggetti [ContextNode](/previous-versions/ms551996(v=vs.100)) specifici, ad esempio [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))e altri, non vengono utilizzati nel livello com.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="4b4f9-128">È invece consigliabile usare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) sull'interfaccia [**IContextNode**](icontextnode.md) standard.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="4b4f9-129">È necessario \# includere "IACom. h".</span><span class="sxs-lookup"><span data-stu-id="4b4f9-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="4b4f9-130">È probabile che le librerie vengano utilizzate insieme all'oggetto input penna della piattaforma Tablet PC, pertanto è necessario \# includere anche "msinkaut. h".</span><span class="sxs-lookup"><span data-stu-id="4b4f9-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="4b4f9-131">RTS e altre applicazioni</span><span class="sxs-lookup"><span data-stu-id="4b4f9-131">RTS and Other Applications</span></span>

<span data-ttu-id="4b4f9-132">Il livello di base dell'analisi dell'input penna funziona in modo diverso rispetto agli altri in quanto accetta dati punto per l'analisi anziché oggetti [Stroke](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="4b4f9-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="4b4f9-133">Esempi di come usare direttamente il livello di base anziché i livelli di Windows Form o COM includono applicazioni che non usano oggetti input penna della piattaforma Tablet PC di prima generazione o applicazioni che usano le API [**RealTimeStylus**](realtimestylus-class.md) per gestire l'input dello stilo anziché usare gli oggetti [input penna](/previous-versions/ms583670(v=vs.100)) della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="4b4f9-134">Solo supporto a 32 bit</span><span class="sxs-lookup"><span data-stu-id="4b4f9-134">32-bit Support Only</span></span>

<span data-ttu-id="4b4f9-135">Si noti che le librerie di analisi dell'input penna sono supportate solo nei processi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4b4f9-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b4f9-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b4f9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b4f9-137">Panoramica dell'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4b4f9-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="4b4f9-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4b4f9-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
