---
description: Imposta una matrice di vettori.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'Metodo ID3DXBaseEffect:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969428"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="0982f-103">Metodo ID3DXBaseEffect:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="0982f-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="0982f-104">Imposta una matrice di vettori.</span><span class="sxs-lookup"><span data-stu-id="0982f-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="0982f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0982f-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="0982f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0982f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0982f-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0982f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0982f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0982f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0982f-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="0982f-109">Unique identifier.</span></span> <span data-ttu-id="0982f-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0982f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0982f-111">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0982f-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0982f-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0982f-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0982f-113">Matrice di vettori di punti a virgola mobile 4D.</span><span class="sxs-lookup"><span data-stu-id="0982f-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="0982f-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0982f-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0982f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0982f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0982f-116">Numero di vettori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0982f-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0982f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0982f-117">Return value</span></span>

<span data-ttu-id="0982f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0982f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0982f-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0982f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0982f-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0982f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0982f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0982f-121">Remarks</span></span>

<span data-ttu-id="0982f-122">Se i vettori di destinazione sono inferiori ai vettori di origine, i componenti aggiuntivi dei vettori di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="0982f-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0982f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0982f-123">Requirements</span></span>



| <span data-ttu-id="0982f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0982f-124">Requirement</span></span> | <span data-ttu-id="0982f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0982f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0982f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0982f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0982f-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0982f-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0982f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="0982f-128">Library</span></span><br/> | <dl> <span data-ttu-id="0982f-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0982f-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0982f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0982f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0982f-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0982f-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0982f-132">**GetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="0982f-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
