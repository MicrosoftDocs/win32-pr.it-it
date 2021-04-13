---
title: Ritaglio (OpenGL)
description: Il ritaglio si verifica in due passaggi
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline di elaborazione OpenGL, ritaglio
- ritaglio di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400131"
---
# <a name="clipping-opengl"></a><span data-ttu-id="d0039-105">Ritaglio (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="d0039-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="d0039-106">Il ritaglio si verifica in due passaggi:</span><span class="sxs-lookup"><span data-stu-id="d0039-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="d0039-107">**Visualizza il ritaglio specifico del volume clippingApplication.**</span><span class="sxs-lookup"><span data-stu-id="d0039-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="d0039-108">Subito dopo aver assemblato le primitive, queste vengono ritagliate in coordinate oculari in base alle esigenze per tutti i piani di ritaglio definiti con [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="d0039-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="d0039-109">OpenGL richiede il supporto per almeno sei piani di ritaglio specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0039-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="d0039-110">Le primitive vengono trasformate dalla matrice di proiezione in coordinate di ritaglio e ritagliate dal volume di visualizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d0039-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="d0039-111">Questa matrice può essere controllata dalle funzioni di trasformazione della matrice (vedere [trasformazioni matrici](matrix-transformations.md)), ma in genere è specificata da [**glFrustum**](glfrustum.md) o [**glOrtho**](glortho.md).</span><span class="sxs-lookup"><span data-stu-id="d0039-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="d0039-112">Punti, segmenti di linea e poligoni vengono gestiti in modo diverso durante il ritaglio:</span><span class="sxs-lookup"><span data-stu-id="d0039-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="d0039-113">I punti vengono conservati nello stato originale (se sono all'interno del volume di ritaglio) o rimossi (se sono all'esterno del volume di ritaglio).</span><span class="sxs-lookup"><span data-stu-id="d0039-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="d0039-114">Se parti di poligoni o segmenti di linea sono all'esterno del volume di ritaglio, i nuovi vertici vengono generati nei punti di clip.</span><span class="sxs-lookup"><span data-stu-id="d0039-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="d0039-115">Per i poligoni, può essere necessario costruire un bordo intero tra i nuovi vertici generati nei punti di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="d0039-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="d0039-116">Per i segmenti di linea e i poligoni che vengono ritagliati, le informazioni relative al flag, al colore e alla trama del bordo vengono assegnate a tutti i nuovi vertici.</span><span class="sxs-lookup"><span data-stu-id="d0039-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




