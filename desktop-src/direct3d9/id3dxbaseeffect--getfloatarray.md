---
description: Ottiene una matrice di valori a virgola mobile.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'Metodo ID3DXBaseEffect:: GetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355919"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="b803a-103">Metodo ID3DXBaseEffect:: GetFloatArray</span><span class="sxs-lookup"><span data-stu-id="b803a-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="b803a-104">Ottiene una matrice di valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b803a-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b803a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b803a-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="b803a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b803a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b803a-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b803a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b803a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b803a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b803a-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="b803a-109">Unique identifier.</span></span> <span data-ttu-id="b803a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b803a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b803a-111">*PF* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b803a-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b803a-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b803a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b803a-113">Restituisce una matrice di valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b803a-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="b803a-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b803a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b803a-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b803a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b803a-116">Numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="b803a-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b803a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b803a-117">Return value</span></span>

<span data-ttu-id="b803a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b803a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b803a-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b803a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b803a-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b803a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b803a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b803a-121">Requirements</span></span>



| <span data-ttu-id="b803a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b803a-122">Requirement</span></span> | <span data-ttu-id="b803a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b803a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b803a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b803a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b803a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b803a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b803a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b803a-126">Library</span></span><br/> | <dl> <span data-ttu-id="b803a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b803a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b803a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b803a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b803a-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b803a-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b803a-130">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="b803a-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
