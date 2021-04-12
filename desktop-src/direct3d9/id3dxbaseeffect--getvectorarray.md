---
description: Ottiene una matrice di vettori.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'Metodo ID3DXBaseEffect:: GetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354124"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="4c8ea-103">Metodo ID3DXBaseEffect:: GetVectorArray</span><span class="sxs-lookup"><span data-stu-id="4c8ea-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="4c8ea-104">Ottiene una matrice di vettori.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c8ea-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="4c8ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c8ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8ea-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c8ea-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8ea-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4c8ea-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4c8ea-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-109">Unique identifier.</span></span> <span data-ttu-id="4c8ea-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="4c8ea-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c8ea-111">*pVector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c8ea-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8ea-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c8ea-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4c8ea-113">Restituisce una matrice di vettori di punti a virgola mobile 4D.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="4c8ea-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4c8ea-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8ea-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c8ea-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c8ea-116">Numero di vettori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8ea-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c8ea-117">Return value</span></span>

<span data-ttu-id="4c8ea-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c8ea-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c8ea-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c8ea-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c8ea-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c8ea-121">Remarks</span></span>

<span data-ttu-id="4c8ea-122">Se i vettori di destinazione sono più grandi dei vettori di origine, verranno riempiti solo i componenti iniziali di ogni vettore di destinazione e i componenti del vettore di destinazione rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="4c8ea-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8ea-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c8ea-123">Requirements</span></span>



| <span data-ttu-id="4c8ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8ea-124">Requirement</span></span> | <span data-ttu-id="4c8ea-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4c8ea-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8ea-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c8ea-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4c8ea-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ea-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4c8ea-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c8ea-128">Library</span></span><br/> | <dl> <span data-ttu-id="4c8ea-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ea-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4c8ea-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c8ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8ea-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="4c8ea-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="4c8ea-132">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="4c8ea-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
