---
description: La posizione, la velocità e l'orientamento delle origini audio e dei listener nello spazio 3D sono rappresentati da coordinate cartesiane, ovvero valori su tre assi, ovvero l'asse x, l'asse y e l'asse z.
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordinate dello spazio 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232297"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="eb96b-103">Coordinate dello spazio 3D</span><span class="sxs-lookup"><span data-stu-id="eb96b-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="eb96b-104">La posizione, la velocità e l'orientamento delle origini audio e dei listener nello spazio 3D sono rappresentati da coordinate cartesiane, ovvero valori su tre assi, ovvero l'asse x, l'asse y e l'asse z.</span><span class="sxs-lookup"><span data-stu-id="eb96b-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="eb96b-105">Gli assi sono relativi a un punto di vista stabilito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb96b-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="eb96b-106">I valori sull'asse x aumentano da sinistra verso destra, sull'asse y da giù verso l'alto e sull'asse z da vicino a lungo.</span><span class="sxs-lookup"><span data-stu-id="eb96b-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="eb96b-107">La **struttura \_ vettoriale X3DAUDIO** contiene valori che descrivono la posizione, la velocità o l'orientamento sui tre assi.</span><span class="sxs-lookup"><span data-stu-id="eb96b-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="eb96b-108">Convenzionalmente, i vettori sono espressi come tre valori racchiusi tra parentesi e separati da virgole, nell'ordine (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="eb96b-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="eb96b-109">Per position, i valori si trovano in unità internazionali definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eb96b-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="eb96b-110">Per velocità, il vettore descrive la frequenza di spostamento lungo ogni asse in unità internazionali al secondo.</span><span class="sxs-lookup"><span data-stu-id="eb96b-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="eb96b-111">Per l'orientamento, i valori sono in unità arbitrarie e sono relativi tra loro.</span><span class="sxs-lookup"><span data-stu-id="eb96b-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="eb96b-112">Ad esempio, se la visualizzazione di base del mondo 3D si trova verso nord verso l'orizzonte e l'orientamento del listener è (-1, 0, 1), il listener viene rivolto a nordovest.</span><span class="sxs-lookup"><span data-stu-id="eb96b-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="eb96b-113">Poiché i valori all'interno di un vettore non sono in unità assolute, il vettore può essere espresso in modo analogo (-5, 0, 5) o (-0,25, 0, 0,25).</span><span class="sxs-lookup"><span data-stu-id="eb96b-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="eb96b-114">i vettori 3D funzionano in modo analogo ai vettori 2D, ma con un asse aggiuntivo nella direzione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="eb96b-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="eb96b-115">È possibile vedere in che modo i vettori funzionano nello spazio 2D disegnando questi ultimi in un foglio grafico.</span><span class="sxs-lookup"><span data-stu-id="eb96b-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="eb96b-116">Lasciare che i valori aumentino dalla parte inferiore alla parte superiore della carta e da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="eb96b-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="eb96b-117">Una linea disegnata da (0,0) a (1,1) ha lo stesso orientamento, o direzione, di uno tracciato da (0, 0) a (5, 5).</span><span class="sxs-lookup"><span data-stu-id="eb96b-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="eb96b-118">Tuttavia, la seconda riga indica una distanza o una velocità maggiore.</span><span class="sxs-lookup"><span data-stu-id="eb96b-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb96b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb96b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb96b-120">Concetti audio comuni</span><span class="sxs-lookup"><span data-stu-id="eb96b-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="eb96b-121">Panoramica di X3DAudio</span><span class="sxs-lookup"><span data-stu-id="eb96b-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



