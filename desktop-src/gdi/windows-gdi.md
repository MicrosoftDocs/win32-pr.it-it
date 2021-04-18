---
description: Microsoft Windows Graphics Device Interface (GDI) consente alle applicazioni di utilizzare grafica e testo formattato sia sullo schermo video che sulla stampante.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: GDI Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979359"
---
# <a name="windows-gdi"></a><span data-ttu-id="5e6d3-103">GDI Windows</span><span class="sxs-lookup"><span data-stu-id="5e6d3-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="5e6d3-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="5e6d3-104">Purpose</span></span>

<span data-ttu-id="5e6d3-105">Microsoft Windows Graphics Device Interface (GDI) consente alle applicazioni di utilizzare grafica e testo formattato sia sullo schermo video che sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="5e6d3-106">Le applicazioni basate su Windows non accedono direttamente all'hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="5e6d3-107">GDI interagisce invece con i driver di dispositivo per conto delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5e6d3-108">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="5e6d3-108">Where applicable</span></span>

<span data-ttu-id="5e6d3-109">GDI può essere usato in tutte le applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5e6d3-110">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="5e6d3-110">Developer audience</span></span>

<span data-ttu-id="5e6d3-111">Questa API è progettata per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="5e6d3-112">È necessaria una certa familiarità con l' [architettura basata su messaggi](../learnwin32/window-messages.md) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5e6d3-113">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="5e6d3-113">Run-time requirements</span></span>

<span data-ttu-id="5e6d3-114">Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione requisiti della documentazione relativa alla funzione.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e6d3-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5e6d3-115">In this section</span></span>

-   [<span data-ttu-id="5e6d3-116">Bitmap</span><span class="sxs-lookup"><span data-stu-id="5e6d3-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="5e6d3-117">Pennelli</span><span class="sxs-lookup"><span data-stu-id="5e6d3-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="5e6d3-118">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="5e6d3-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="5e6d3-119">Colori</span><span class="sxs-lookup"><span data-stu-id="5e6d3-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="5e6d3-120">Spazi di coordinate e trasformazioni</span><span class="sxs-lookup"><span data-stu-id="5e6d3-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="5e6d3-121">Contesti di dispositivo</span><span class="sxs-lookup"><span data-stu-id="5e6d3-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="5e6d3-122">Forme piene</span><span class="sxs-lookup"><span data-stu-id="5e6d3-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="5e6d3-123">Tipi di carattere e testo</span><span class="sxs-lookup"><span data-stu-id="5e6d3-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="5e6d3-124">Linee e curve</span><span class="sxs-lookup"><span data-stu-id="5e6d3-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="5e6d3-125">Metafile</span><span class="sxs-lookup"><span data-stu-id="5e6d3-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="5e6d3-126">Più monitor di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="5e6d3-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="5e6d3-127">Disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="5e6d3-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="5e6d3-128">Percorsi</span><span class="sxs-lookup"><span data-stu-id="5e6d3-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="5e6d3-129">Penne</span><span class="sxs-lookup"><span data-stu-id="5e6d3-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="5e6d3-130">[Stampa e spooler di stampa](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e6d3-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="5e6d3-131">Rettangoli</span><span class="sxs-lookup"><span data-stu-id="5e6d3-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="5e6d3-132">Aree</span><span class="sxs-lookup"><span data-stu-id="5e6d3-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="5e6d3-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e6d3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e6d3-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="5e6d3-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="5e6d3-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="5e6d3-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="5e6d3-136">OpenGL</span><span class="sxs-lookup"><span data-stu-id="5e6d3-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="5e6d3-137">Acquisizione di immagini Windows</span><span class="sxs-lookup"><span data-stu-id="5e6d3-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
