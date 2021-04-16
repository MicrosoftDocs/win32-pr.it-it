---
description: Motore di rendering di base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motore di rendering di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522218"
---
# <a name="basic-render-engine"></a><span data-ttu-id="04c19-103">Motore di rendering di base</span><span class="sxs-lookup"><span data-stu-id="04c19-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="04c19-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04c19-104">\[Deprecated.</span></span> <span data-ttu-id="04c19-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04c19-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04c19-106">L'oggetto motore di rendering di base esegue il rendering dell'output non compresso da una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="04c19-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="04c19-107">Per creare questo oggetto, chiamare **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="04c19-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="04c19-108">Per l'output compresso, usare il motore di rendering intelligente.</span><span class="sxs-lookup"><span data-stu-id="04c19-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="04c19-109">L'identificatore di classe è CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="04c19-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="04c19-110">Il motore di rendering di base espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="04c19-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="04c19-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="04c19-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="04c19-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="04c19-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="04c19-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="04c19-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="04c19-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="04c19-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="04c19-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04c19-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c19-116">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="04c19-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="04c19-117">Motore di rendering intelligente</span><span class="sxs-lookup"><span data-stu-id="04c19-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



