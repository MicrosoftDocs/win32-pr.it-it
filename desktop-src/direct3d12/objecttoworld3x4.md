---
description: 'ObjectToWorld3x4: matrice per la trasformazione dallo spazio oggetti allo spazio globale.'
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107739"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="d89bb-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="d89bb-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="d89bb-104">Matrice per la trasformazione da spazio oggetto a spazio del mondo.</span><span class="sxs-lookup"><span data-stu-id="d89bb-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="d89bb-105">Lo spazio oggetto si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.</span><span class="sxs-lookup"><span data-stu-id="d89bb-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89bb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d89bb-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="d89bb-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d89bb-107">Remarks</span></span>

<span data-ttu-id="d89bb-108">La matrice è una trasposizione **della matrice ObjectToWorld4x3.**</span><span class="sxs-lookup"><span data-stu-id="d89bb-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="d89bb-109">Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:</span><span class="sxs-lookup"><span data-stu-id="d89bb-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="d89bb-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="d89bb-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="d89bb-111">**Hit Shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="d89bb-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="d89bb-112">**Shader di intersezione**</span><span class="sxs-lookup"><span data-stu-id="d89bb-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="d89bb-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89bb-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89bb-114">Informazioni di riferimento su Direct3D 12 Raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="d89bb-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




