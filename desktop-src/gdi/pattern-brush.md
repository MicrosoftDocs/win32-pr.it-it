---
description: Un pennello modello (o personalizzato) viene creato da una bitmap definita dall'applicazione o da una bitmap indipendente dal dispositivo (DIB). I rettangoli seguenti sono stati disegnati usando pennelli modello diversi.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pennello per pattern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987872"
---
# <a name="pattern-brush"></a><span data-ttu-id="b2bf2-104">Pennello per pattern</span><span class="sxs-lookup"><span data-stu-id="b2bf2-104">Pattern Brush</span></span>

<span data-ttu-id="b2bf2-105">Un pennello modello (o personalizzato) viene creato da una bitmap definita dall'applicazione o da una bitmap indipendente dal dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="b2bf2-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="b2bf2-106">I rettangoli seguenti sono stati disegnati usando pennelli modello diversi.</span><span class="sxs-lookup"><span data-stu-id="b2bf2-106">The following rectangles were painted by using different pattern brushes.</span></span>

![illustrazione che mostra tre caselle, ognuna con un modello diverso](images/csbru-05.png)

<span data-ttu-id="b2bf2-108">Per creare un pennello logico, un'applicazione deve prima creare una bitmap.</span><span class="sxs-lookup"><span data-stu-id="b2bf2-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="b2bf2-109">Dopo la creazione della bitmap, l'applicazione può creare il pennello logico chiamando la funzione [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) o [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , fornendo un handle che identifica la bitmap (o DIB).</span><span class="sxs-lookup"><span data-stu-id="b2bf2-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="b2bf2-110">I pennelli visualizzati nell'illustrazione precedente sono stati creati da bitmap monocromatiche.</span><span class="sxs-lookup"><span data-stu-id="b2bf2-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="b2bf2-111">Per una descrizione delle bitmap, delle DIB e delle funzioni che li creano, vedere [bitmap](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="b2bf2-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



