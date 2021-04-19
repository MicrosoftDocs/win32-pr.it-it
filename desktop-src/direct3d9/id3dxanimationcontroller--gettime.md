---
description: Ottiene il tempo di animazione globale.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'Metodo ID3DXAnimationController:: getTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323058"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="8838f-103">Metodo ID3DXAnimationController:: getTime</span><span class="sxs-lookup"><span data-stu-id="8838f-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="8838f-104">Ottiene il tempo di animazione globale.</span><span class="sxs-lookup"><span data-stu-id="8838f-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8838f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8838f-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="8838f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8838f-106">Parameters</span></span>

<span data-ttu-id="8838f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8838f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8838f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8838f-108">Return value</span></span>

<span data-ttu-id="8838f-109">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8838f-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8838f-110">Restituisce il tempo di animazione globale.</span><span class="sxs-lookup"><span data-stu-id="8838f-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="8838f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8838f-111">Remarks</span></span>

<span data-ttu-id="8838f-112">Le animazioni sono progettate usando un'ora di animazione locale e vengono combinate in tempi globali con [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="8838f-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8838f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8838f-113">Requirements</span></span>



| <span data-ttu-id="8838f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8838f-114">Requirement</span></span> | <span data-ttu-id="8838f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8838f-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8838f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8838f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8838f-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8838f-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8838f-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="8838f-118">Library</span></span><br/> | <dl> <span data-ttu-id="8838f-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8838f-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8838f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8838f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8838f-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8838f-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
