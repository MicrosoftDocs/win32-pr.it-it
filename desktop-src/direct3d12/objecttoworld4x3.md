---
description: 'ObjectToWorld4x3: matrice per la trasformazione dallo spazio oggetti allo spazio globale.'
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098299"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="a9003-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="a9003-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="a9003-104">Matrice per la trasformazione dallo spazio oggetti allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="a9003-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="a9003-105">Lo spazio oggetti si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.</span><span class="sxs-lookup"><span data-stu-id="a9003-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9003-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9003-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="a9003-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a9003-107">Remarks</span></span>

<span data-ttu-id="a9003-108">La matrice è una trasposizione della **matrice ObjectToWorld3x4.**</span><span class="sxs-lookup"><span data-stu-id="a9003-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="a9003-109">Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9003-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="a9003-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="a9003-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="a9003-111">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="a9003-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="a9003-112">**Intersection Shader**</span><span class="sxs-lookup"><span data-stu-id="a9003-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="a9003-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9003-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9003-114">Informazioni di riferimento su HLSL per Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="a9003-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




