---
description: Ottiene un set di animazioni.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'Metodo ID3DXAnimationController:: getanimationt (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132366"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="f7900-103">Metodo ID3DXAnimationController:: getanimationt</span><span class="sxs-lookup"><span data-stu-id="f7900-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="f7900-104">Ottiene un set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="f7900-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7900-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7900-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="f7900-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7900-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f7900-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7900-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7900-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7900-109">Indice del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="f7900-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="f7900-110">*ppAnimSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f7900-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7900-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7900-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="f7900-112">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="f7900-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7900-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7900-113">Return value</span></span>

<span data-ttu-id="f7900-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7900-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7900-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7900-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f7900-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f7900-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7900-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7900-117">Remarks</span></span>

<span data-ttu-id="f7900-118">Il controller di animazione contiene una matrice di set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="f7900-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="f7900-119">Questo metodo restituisce uno di essi in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f7900-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7900-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7900-120">Requirements</span></span>



| <span data-ttu-id="f7900-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7900-121">Requirement</span></span> | <span data-ttu-id="f7900-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f7900-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7900-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7900-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f7900-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7900-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f7900-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7900-125">Library</span></span><br/> | <dl> <span data-ttu-id="f7900-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7900-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7900-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7900-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7900-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f7900-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
