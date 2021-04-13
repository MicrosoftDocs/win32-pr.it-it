---
description: Ottiene una matrice trasposta.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'Metodo ID3DXBaseEffect:: GetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355889"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="74c0a-103">Metodo ID3DXBaseEffect:: GetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="74c0a-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="74c0a-104">Ottiene una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="74c0a-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c0a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74c0a-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="74c0a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74c0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c0a-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c0a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="74c0a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="74c0a-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="74c0a-109">Unique identifier.</span></span> <span data-ttu-id="74c0a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="74c0a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="74c0a-111">*pmatrix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c0a-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="74c0a-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74c0a-113">Restituisce una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="74c0a-113">Returns a transposed matrix.</span></span> <span data-ttu-id="74c0a-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="74c0a-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c0a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74c0a-115">Return value</span></span>

<span data-ttu-id="74c0a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74c0a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74c0a-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74c0a-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74c0a-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="74c0a-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c0a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="74c0a-119">Remarks</span></span>

<span data-ttu-id="74c0a-120">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="74c0a-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="74c0a-121">Se la matrice di destinazione è più grande della matrice di origine, verranno riempiti solo gli elementi in alto a sinistra della matrice di destinazione e i componenti della matrice di destinazione rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="74c0a-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="74c0a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74c0a-122">Requirements</span></span>



| <span data-ttu-id="74c0a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="74c0a-123">Requirement</span></span> | <span data-ttu-id="74c0a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="74c0a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c0a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74c0a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="74c0a-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="74c0a-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="74c0a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="74c0a-127">Library</span></span><br/> | <dl> <span data-ttu-id="74c0a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74c0a-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="74c0a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74c0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c0a-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="74c0a-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="74c0a-131">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="74c0a-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




