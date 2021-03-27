---
description: I record spline rappresentano le curve quadratiche (ovvero le spline b quadratiche) utilizzate da TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Record spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755839"
---
# <a name="spline-records"></a><span data-ttu-id="b4278-103">Record spline</span><span class="sxs-lookup"><span data-stu-id="b4278-103">Spline Records</span></span>

<span data-ttu-id="b4278-104">I record spline rappresentano le curve quadratiche (ovvero le spline b quadratiche) utilizzate da TrueType.</span><span class="sxs-lookup"><span data-stu-id="b4278-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="b4278-105">Un record spline inizia con l'ultimo punto del record precedente (o per il primo record nel contorno con il punto iniziale).</span><span class="sxs-lookup"><span data-stu-id="b4278-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="b4278-106">Per il primo record spline, il punto iniziale e l'ultimo punto del record si trovano sulla struttura del glifo.</span><span class="sxs-lookup"><span data-stu-id="b4278-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="b4278-107">Per tutti gli altri record spline, solo l'ultimo punto si trova nella struttura del glifo.</span><span class="sxs-lookup"><span data-stu-id="b4278-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="b4278-108">Tutti gli altri punti nei record della spline si trovano fuori dal contorno del glifo ed è necessario eseguirne il rendering come punti di controllo di b-spline.</span><span class="sxs-lookup"><span data-stu-id="b4278-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="b4278-109">L'ultimo record spline o polilinea in un contorno termina sempre con il punto iniziale del contorno.</span><span class="sxs-lookup"><span data-stu-id="b4278-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="b4278-110">Questa disposizione garantisce la chiusura di ogni contorno.</span><span class="sxs-lookup"><span data-stu-id="b4278-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="b4278-111">Poiché le spline b richiedono tre punti (un punto fuori dal contorno del glifo tra due punti che si trovano sulla struttura), è necessario eseguire alcuni calcoli quando un record spline contiene più di un punto fuori curva.</span><span class="sxs-lookup"><span data-stu-id="b4278-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="b4278-112">Se, ad esempio, un record spline contiene tre punti (A, B e C) e non è il primo record, i punti A e B sono fuori dal contorno del glifo.</span><span class="sxs-lookup"><span data-stu-id="b4278-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="b4278-113">Per interpretare il punto A, usare la posizione corrente (che è sempre sul contorno del glifo) e il punto sulla struttura del glifo tra i punti A e B. Per trovare il punto medio (M) tra A e B, è possibile eseguire il calcolo seguente.</span><span class="sxs-lookup"><span data-stu-id="b4278-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="b4278-114">M = A + (B A)/2</span><span class="sxs-lookup"><span data-stu-id="b4278-114">M = A + (B A)/2</span></span>

<span data-ttu-id="b4278-115">Il punto medio tra i punti fuori struttura consecutivi in un record spline è un punto del contorno del glifo, in base alla definizione del formato spline usato nei tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="b4278-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="b4278-116">Se la posizione corrente è designata da P, le due spline quadratiche definite da questo record spline sono (P, A, M) e (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="b4278-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



