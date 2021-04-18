---
description: Aggiunge un set di animazioni al controller dell'animazione.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'Metodo ID3DXAnimationController:: RegisterAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323288"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="554ab-103">Metodo ID3DXAnimationController:: RegisterAnimationSet</span><span class="sxs-lookup"><span data-stu-id="554ab-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="554ab-104">Aggiunge un set di animazioni al controller dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="554ab-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="554ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="554ab-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="554ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="554ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554ab-107">*pAnimSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="554ab-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554ab-108">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="554ab-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="554ab-109">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="554ab-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="554ab-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="554ab-110">Return value</span></span>

<span data-ttu-id="554ab-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="554ab-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="554ab-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="554ab-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="554ab-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="554ab-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="554ab-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="554ab-114">Requirements</span></span>



| <span data-ttu-id="554ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="554ab-115">Requirement</span></span> | <span data-ttu-id="554ab-116">Valore</span><span class="sxs-lookup"><span data-stu-id="554ab-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="554ab-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="554ab-117">Header</span></span><br/>  | <dl> <span data-ttu-id="554ab-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="554ab-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="554ab-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="554ab-119">Library</span></span><br/> | <dl> <span data-ttu-id="554ab-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="554ab-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="554ab-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="554ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554ab-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="554ab-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




