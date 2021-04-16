---
title: Modalità mantenuta rispetto alla modalità immediata
description: Le API grafiche possono essere divise in API in modalità mantenuta e in modalità immediata.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551441"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="5be47-103">Modalità mantenuta rispetto alla modalità immediata</span><span class="sxs-lookup"><span data-stu-id="5be47-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="5be47-104">Le API grafiche possono essere divise in API in *modalità mantenuta* e in *modalità immediata* .</span><span class="sxs-lookup"><span data-stu-id="5be47-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="5be47-105">Direct2D è un'API in modalità immediata.</span><span class="sxs-lookup"><span data-stu-id="5be47-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="5be47-106">Windows Presentation Foundation (WPF) è un esempio di un'API in modalità mantenuta.</span><span class="sxs-lookup"><span data-stu-id="5be47-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="5be47-107">Un'API in modalità mantenuta è dichiarativa.</span><span class="sxs-lookup"><span data-stu-id="5be47-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="5be47-108">L'applicazione crea una scena dalle primitive grafiche, ad esempio forme e linee.</span><span class="sxs-lookup"><span data-stu-id="5be47-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="5be47-109">La libreria grafica archivia un modello della scena in memoria.</span><span class="sxs-lookup"><span data-stu-id="5be47-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="5be47-110">Per disegnare un frame, la libreria grafica trasforma la scena in un set di comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="5be47-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="5be47-111">Tra i frame, la libreria grafica mantiene la scena in memoria.</span><span class="sxs-lookup"><span data-stu-id="5be47-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="5be47-112">Per modificare gli elementi di cui viene eseguito il rendering, l'applicazione emette un comando per aggiornare la scena, ad esempio per aggiungere o rimuovere una forma.</span><span class="sxs-lookup"><span data-stu-id="5be47-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="5be47-113">La libreria è quindi responsabile del ridisegno della scena.</span><span class="sxs-lookup"><span data-stu-id="5be47-113">The library is then responsible for redrawing the scene.</span></span>

![diagramma che mostra la grafica in modalità mantenuta.](images/graphics06.png)

<span data-ttu-id="5be47-115">Un'API in modalità immediata è procedurale.</span><span class="sxs-lookup"><span data-stu-id="5be47-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="5be47-116">Ogni volta che viene disegnato un nuovo frame, l'applicazione invia direttamente i comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="5be47-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="5be47-117">La libreria grafica non archivia un modello di scena tra i frame.</span><span class="sxs-lookup"><span data-stu-id="5be47-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="5be47-118">Al contrario, l'applicazione tiene traccia della scena.</span><span class="sxs-lookup"><span data-stu-id="5be47-118">Instead, the application keeps track of the scene.</span></span>

![diagramma che mostra la grafica in modalità immediata.](images/graphics07.png)

<span data-ttu-id="5be47-120">Le API in modalità mantenuta possono essere più semplici da usare, perché l'API esegue più attività, ad esempio l'inizializzazione, la manutenzione dello stato e la pulizia.</span><span class="sxs-lookup"><span data-stu-id="5be47-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="5be47-121">D'altra parte, sono spesso meno flessibili, perché l'API impone il proprio modello di scena.</span><span class="sxs-lookup"><span data-stu-id="5be47-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="5be47-122">Inoltre, un'API in modalità mantenuta può disporre di requisiti di memoria più elevati, perché deve fornire un modello di scena di uso generale.</span><span class="sxs-lookup"><span data-stu-id="5be47-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="5be47-123">Con un'API in modalità immediata, è possibile implementare le ottimizzazioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5be47-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="5be47-124">Prossima</span><span class="sxs-lookup"><span data-stu-id="5be47-124">Next</span></span>

[<span data-ttu-id="5be47-125">Primo programma Direct2D</span><span class="sxs-lookup"><span data-stu-id="5be47-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




