---
description: Ottiene una matrice di numeri interi.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'Metodo ID3DXBaseEffect:: GetIntArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355899"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="5bb03-103">Metodo ID3DXBaseEffect:: GetIntArray</span><span class="sxs-lookup"><span data-stu-id="5bb03-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="5bb03-104">Ottiene una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="5bb03-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bb03-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5bb03-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bb03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb03-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bb03-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb03-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5bb03-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5bb03-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="5bb03-109">Unique identifier.</span></span> <span data-ttu-id="5bb03-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5bb03-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bb03-111">*PN* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bb03-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb03-112">Tipo: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5bb03-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5bb03-113">Restituisce una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="5bb03-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="5bb03-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5bb03-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb03-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bb03-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bb03-116">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="5bb03-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb03-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bb03-117">Return value</span></span>

<span data-ttu-id="5bb03-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bb03-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bb03-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5bb03-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5bb03-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5bb03-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb03-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bb03-121">Requirements</span></span>



| <span data-ttu-id="5bb03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb03-122">Requirement</span></span> | <span data-ttu-id="5bb03-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5bb03-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb03-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bb03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5bb03-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb03-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5bb03-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5bb03-126">Library</span></span><br/> | <dl> <span data-ttu-id="5bb03-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bb03-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5bb03-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bb03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb03-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5bb03-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5bb03-130">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="5bb03-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 
