---
description: Matrice per la trasformazione da spazio globale a oggetto-spazio.
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305310"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="7438c-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="7438c-103">WorldToObject3x4</span></span>

<span data-ttu-id="7438c-104">Matrice per la trasformazione da spazio globale a oggetto-spazio.</span><span class="sxs-lookup"><span data-stu-id="7438c-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="7438c-105">Oggetto-spazio si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.</span><span class="sxs-lookup"><span data-stu-id="7438c-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7438c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7438c-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="7438c-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7438c-107">Remarks</span></span>

<span data-ttu-id="7438c-108">La matrice è una trasposizione della matrice **WorldToObject4x3** .</span><span class="sxs-lookup"><span data-stu-id="7438c-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="7438c-109">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="7438c-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="7438c-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="7438c-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="7438c-111">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="7438c-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="7438c-112">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="7438c-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="7438c-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7438c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7438c-114">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="7438c-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




