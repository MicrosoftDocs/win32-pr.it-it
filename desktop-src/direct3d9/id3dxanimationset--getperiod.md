---
description: Ottiene il periodo del set di animazioni.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Metodo ID3DXAnimationSet:: GetPeriod (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323620"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="e41ff-103">Metodo ID3DXAnimationSet:: GetPeriod</span><span class="sxs-lookup"><span data-stu-id="e41ff-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="e41ff-104">Ottiene il periodo del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="e41ff-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e41ff-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="e41ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e41ff-106">Parameters</span></span>

<span data-ttu-id="e41ff-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e41ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e41ff-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e41ff-108">Return value</span></span>

<span data-ttu-id="e41ff-109">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41ff-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e41ff-110">Periodo del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="e41ff-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41ff-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e41ff-111">Remarks</span></span>

<span data-ttu-id="e41ff-112">Il periodo è l'intervallo di tempo in cui i fotogrammi chiave dell'animazione sono validi.</span><span class="sxs-lookup"><span data-stu-id="e41ff-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="e41ff-113">Per le animazioni di ciclo, questo è il periodo del ciclo.</span><span class="sxs-lookup"><span data-stu-id="e41ff-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="e41ff-114">Le unità di tempo in cui sono specificati i fotogrammi chiave (ad esempio, secondi) sono determinate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e41ff-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41ff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e41ff-115">Requirements</span></span>



| <span data-ttu-id="e41ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41ff-116">Requirement</span></span> | <span data-ttu-id="e41ff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e41ff-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41ff-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e41ff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e41ff-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41ff-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e41ff-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e41ff-120">Library</span></span><br/> | <dl> <span data-ttu-id="e41ff-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e41ff-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e41ff-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e41ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41ff-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e41ff-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
