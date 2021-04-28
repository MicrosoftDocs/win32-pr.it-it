---
description: 'WorldToObject4x3: matrice per la trasformazione dallo spazio del mondo allo spazio oggetto.'
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105248"
---
# <a name="worldtoobject4x3"></a><span data-ttu-id="1c62f-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="1c62f-103">WorldToObject4x3</span></span>

<span data-ttu-id="1c62f-104">Matrice per la trasformazione da spazio del mondo a spazio oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c62f-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="1c62f-105">Lo spazio oggetto si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.</span><span class="sxs-lookup"><span data-stu-id="1c62f-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c62f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c62f-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="1c62f-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1c62f-107">Remarks</span></span>

<span data-ttu-id="1c62f-108">La matrice è una trasposizione **della matrice WorldToObject3x4.**</span><span class="sxs-lookup"><span data-stu-id="1c62f-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="1c62f-109">Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:</span><span class="sxs-lookup"><span data-stu-id="1c62f-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="1c62f-110">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="1c62f-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="1c62f-111">**Hit Shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="1c62f-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="1c62f-112">**Shader di intersezione**</span><span class="sxs-lookup"><span data-stu-id="1c62f-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="1c62f-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c62f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c62f-114">Informazioni di riferimento su Direct3D 12 Raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="1c62f-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




