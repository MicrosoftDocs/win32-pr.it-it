---
description: Ottiene un set di animazioni, dato il relativo nome.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'Metodo ID3DXAnimationController:: GetAnimationSetByName (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323176"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="998c7-103">Metodo ID3DXAnimationController:: GetAnimationSetByName</span><span class="sxs-lookup"><span data-stu-id="998c7-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="998c7-104">Ottiene un set di animazioni, dato il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="998c7-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="998c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="998c7-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="998c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="998c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c7-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="998c7-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="998c7-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="998c7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="998c7-109">Stringa contenente il nome del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="998c7-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="998c7-110">*ppAnimSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="998c7-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="998c7-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="998c7-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="998c7-112">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="998c7-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="998c7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="998c7-113">Return value</span></span>

<span data-ttu-id="998c7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="998c7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="998c7-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="998c7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="998c7-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="998c7-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="998c7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="998c7-117">Remarks</span></span>

<span data-ttu-id="998c7-118">Il controller di animazione contiene una matrice di set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="998c7-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="998c7-119">Questo metodo restituisce un set di animazioni con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="998c7-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="998c7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="998c7-120">Requirements</span></span>



| <span data-ttu-id="998c7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="998c7-121">Requirement</span></span> | <span data-ttu-id="998c7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="998c7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="998c7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="998c7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="998c7-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="998c7-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="998c7-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="998c7-125">Library</span></span><br/> | <dl> <span data-ttu-id="998c7-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="998c7-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="998c7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="998c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998c7-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="998c7-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
