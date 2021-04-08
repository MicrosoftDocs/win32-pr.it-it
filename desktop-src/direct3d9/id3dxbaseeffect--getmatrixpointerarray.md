---
description: Ottiene una matrice di puntatori alle matrici nontransposed.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'Metodo ID3DXBaseEffect:: GetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969507"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="c516b-103">Metodo ID3DXBaseEffect:: GetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="c516b-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="c516b-104">Ottiene una matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="c516b-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c516b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c516b-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c516b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c516b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c516b-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c516b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c516b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c516b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c516b-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="c516b-109">Unique identifier.</span></span> <span data-ttu-id="c516b-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c516b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c516b-111">*ppMatrix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c516b-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c516b-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c516b-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="c516b-113">Matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="c516b-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="c516b-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c516b-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c516b-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c516b-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c516b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c516b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c516b-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="c516b-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c516b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c516b-118">Return value</span></span>

<span data-ttu-id="c516b-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c516b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c516b-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c516b-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c516b-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c516b-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c516b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c516b-122">Remarks</span></span>

<span data-ttu-id="c516b-123">Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="c516b-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="c516b-124">Se le matrici di destinazione sono più grandi delle matrici di origine, verranno riempiti solo i componenti in alto a sinistra di ogni matrice di destinazione e i componenti della matrice di destinazione rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="c516b-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c516b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c516b-125">Requirements</span></span>



| <span data-ttu-id="c516b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c516b-126">Requirement</span></span> | <span data-ttu-id="c516b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c516b-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c516b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c516b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c516b-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c516b-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c516b-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="c516b-130">Library</span></span><br/> | <dl> <span data-ttu-id="c516b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c516b-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c516b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c516b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c516b-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c516b-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c516b-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="c516b-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
