---
description: Motore di rendering intelligente
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Motore di rendering intelligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304170"
---
# <a name="smart-render-engine"></a><span data-ttu-id="57ac0-103">Motore di rendering intelligente</span><span class="sxs-lookup"><span data-stu-id="57ac0-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="57ac0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="57ac0-104">\[Deprecated.</span></span> <span data-ttu-id="57ac0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57ac0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57ac0-106">L'oggetto motore di rendering intelligente esegue il rendering dell'output compresso da una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="57ac0-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="57ac0-107">Per creare questo oggetto, chiamare **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="57ac0-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="57ac0-108">Per l'output non compresso, usare il motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="57ac0-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="57ac0-109">L'identificatore di classe è CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="57ac0-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="57ac0-110">Il motore di rendering intelligente espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="57ac0-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="57ac0-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="57ac0-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="57ac0-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="57ac0-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="57ac0-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="57ac0-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="57ac0-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="57ac0-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="57ac0-115">**ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="57ac0-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="57ac0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57ac0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ac0-117">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="57ac0-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="57ac0-118">Motore di rendering di base</span><span class="sxs-lookup"><span data-stu-id="57ac0-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 



