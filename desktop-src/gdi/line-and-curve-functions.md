---
description: Le funzioni seguenti vengono usate con linee e curve.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Funzioni linea e curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993944"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="d9866-103">Funzioni linea e curva</span><span class="sxs-lookup"><span data-stu-id="d9866-103">Line and Curve Functions</span></span>

<span data-ttu-id="d9866-104">Le funzioni seguenti vengono usate con linee e curve.</span><span class="sxs-lookup"><span data-stu-id="d9866-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="d9866-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="d9866-105">Function</span></span>                                   | <span data-ttu-id="d9866-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9866-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9866-107">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="d9866-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="d9866-108">Disegna un segmento di linea e un arco.</span><span class="sxs-lookup"><span data-stu-id="d9866-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="d9866-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="d9866-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="d9866-110">Disegna un arco ellittico.</span><span class="sxs-lookup"><span data-stu-id="d9866-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="d9866-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="d9866-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="d9866-112">Disegna un arco ellittico.</span><span class="sxs-lookup"><span data-stu-id="d9866-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="d9866-113">**GetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="d9866-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="d9866-114">Recupera la direzione di arco corrente per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="d9866-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="d9866-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="d9866-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="d9866-116">Determina i pixel da evidenziare per una linea definita dai punti iniziale e finale specificati.</span><span class="sxs-lookup"><span data-stu-id="d9866-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="d9866-117">**LineDDAProc**</span><span class="sxs-lookup"><span data-stu-id="d9866-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="d9866-118">Funzione di callback definita dall'applicazione utilizzata con la funzione LineDDA.</span><span class="sxs-lookup"><span data-stu-id="d9866-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="d9866-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="d9866-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="d9866-120">Disegna una linea dalla posizione corrente fino a, ma non include, il punto specificato.</span><span class="sxs-lookup"><span data-stu-id="d9866-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="d9866-121">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="d9866-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="d9866-122">Aggiorna la posizione corrente al punto specificato e, facoltativamente, restituisce la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="d9866-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="d9866-123">**Polibezier**</span><span class="sxs-lookup"><span data-stu-id="d9866-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="d9866-124">Disegna una o più curve di Bézier.</span><span class="sxs-lookup"><span data-stu-id="d9866-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="d9866-125">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="d9866-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="d9866-126">Disegna una o più curve di Bézier.</span><span class="sxs-lookup"><span data-stu-id="d9866-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="d9866-127">**Polidisegni**</span><span class="sxs-lookup"><span data-stu-id="d9866-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="d9866-128">Disegna un set di segmenti di linea e curve di Bézier.</span><span class="sxs-lookup"><span data-stu-id="d9866-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="d9866-129">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="d9866-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="d9866-130">Disegna una serie di segmenti di linea connettendo i punti nella matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="d9866-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="d9866-131">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="d9866-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="d9866-132">Disegna una o più linee rette.</span><span class="sxs-lookup"><span data-stu-id="d9866-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="d9866-133">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="d9866-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="d9866-134">Disegna più serie di segmenti di linea collegati.</span><span class="sxs-lookup"><span data-stu-id="d9866-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="d9866-135">**SetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="d9866-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="d9866-136">Imposta la direzione di disegno da utilizzare per le funzioni arco e rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d9866-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



