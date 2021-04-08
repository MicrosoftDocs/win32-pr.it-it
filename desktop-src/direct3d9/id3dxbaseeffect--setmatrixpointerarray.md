---
description: Imposta una matrice di puntatori alle matrici nontransposed.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Metodo ID3DXBaseEffect:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969298"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="92352-103">Metodo ID3DXBaseEffect:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="92352-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="92352-104">Imposta una matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="92352-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="92352-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92352-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="92352-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92352-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92352-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92352-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="92352-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="92352-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="92352-109">Unique identifier.</span></span> <span data-ttu-id="92352-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="92352-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="92352-111">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92352-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92352-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="92352-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="92352-113">Matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="92352-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="92352-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="92352-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="92352-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="92352-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92352-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92352-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92352-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="92352-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92352-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92352-118">Return value</span></span>

<span data-ttu-id="92352-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92352-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92352-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92352-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92352-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="92352-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="92352-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="92352-122">Remarks</span></span>

<span data-ttu-id="92352-123">Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="92352-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="92352-124">Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="92352-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="92352-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92352-125">Requirements</span></span>



| <span data-ttu-id="92352-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="92352-126">Requirement</span></span> | <span data-ttu-id="92352-127">Valore</span><span class="sxs-lookup"><span data-stu-id="92352-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92352-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92352-128">Header</span></span><br/>  | <dl> <span data-ttu-id="92352-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="92352-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="92352-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="92352-130">Library</span></span><br/> | <dl> <span data-ttu-id="92352-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92352-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92352-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92352-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92352-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="92352-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="92352-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="92352-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
