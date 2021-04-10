---
description: Estende le applicazioni scritte utilizzando tecnologie basate su COM.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: COM+ (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966108"
---
# <a name="com-component-services"></a><span data-ttu-id="630c8-103">COM+ (Servizi componenti)</span><span class="sxs-lookup"><span data-stu-id="630c8-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="630c8-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="630c8-104">Purpose</span></span>

<span data-ttu-id="630c8-105">COM+ è un'evoluzione di Microsoft Component Object Model (COM) e Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="630c8-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="630c8-106">COM+ si basa su ed estende le applicazioni scritte utilizzando COM, MTS e altre tecnologie basate su COM.</span><span class="sxs-lookup"><span data-stu-id="630c8-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="630c8-107">COM+ gestisce molte delle attività di gestione delle risorse che in precedenza era necessario programmare, ad esempio l'allocazione e la sicurezza dei thread.</span><span class="sxs-lookup"><span data-stu-id="630c8-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="630c8-108">COM+ rende inoltre più scalabili le applicazioni fornendo pool di thread, pool di oggetti e attivazione di oggetti JIT.</span><span class="sxs-lookup"><span data-stu-id="630c8-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="630c8-109">COM+ consente inoltre di proteggere l'integrità dei dati fornendo supporto delle transazioni, anche se una transazione si estende su più database in una rete.</span><span class="sxs-lookup"><span data-stu-id="630c8-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="630c8-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="630c8-110">Where applicable</span></span>

<span data-ttu-id="630c8-111">COM+ può essere utilizzato per sviluppare applicazioni distribuite, mission-critical e di livello aziendale per Windows.</span><span class="sxs-lookup"><span data-stu-id="630c8-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="630c8-112">Se si è un amministratore di sistema, verranno installate, distribuite e configurate le applicazioni COM+ e i relativi componenti.</span><span class="sxs-lookup"><span data-stu-id="630c8-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="630c8-113">Gli sviluppatori di applicazioni possono scrivere componenti e integrarli come applicazioni.</span><span class="sxs-lookup"><span data-stu-id="630c8-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="630c8-114">Se si è un fornitore di strumenti, sarà possibile sviluppare o modificare gli strumenti per lavorare nell'ambiente COM+.</span><span class="sxs-lookup"><span data-stu-id="630c8-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="630c8-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="630c8-115">Developer audience</span></span>

<span data-ttu-id="630c8-116">COM+ è progettato principalmente per gli sviluppatori di Microsoft Visual C++ e Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="630c8-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="630c8-117">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="630c8-117">Run-time requirements</span></span>

<span data-ttu-id="630c8-118">La versione COM+ 1,5 è inclusa in Windows a partire da Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="630c8-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="630c8-119">La versione COM+ 1,0 è inclusa in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="630c8-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="630c8-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="630c8-120">In this section</span></span>

-   [<span data-ttu-id="630c8-121">Novità di COM+ 1,5</span><span class="sxs-lookup"><span data-stu-id="630c8-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="630c8-122">Panoramica degli sviluppatori COM+</span><span class="sxs-lookup"><span data-stu-id="630c8-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="630c8-123">Servizi COM+</span><span class="sxs-lookup"><span data-stu-id="630c8-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="630c8-124">Attività generali COM+</span><span class="sxs-lookup"><span data-stu-id="630c8-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="630c8-125">Riferimento COM+</span><span class="sxs-lookup"><span data-stu-id="630c8-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="630c8-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="630c8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630c8-127">COM</span><span class="sxs-lookup"><span data-stu-id="630c8-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
