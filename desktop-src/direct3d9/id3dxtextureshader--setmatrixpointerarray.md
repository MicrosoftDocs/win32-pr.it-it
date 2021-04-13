---
description: Imposta una matrice di puntatori a matrici non trasposte.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'Metodo ID3DXTextureShader:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354494"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="e1427-103">Metodo ID3DXTextureShader:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="e1427-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="e1427-104">Imposta una matrice di puntatori a matrici non trasposte.</span><span class="sxs-lookup"><span data-stu-id="e1427-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1427-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1427-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="e1427-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1427-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1427-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1427-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e1427-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e1427-109">Identificatore univoco di una matrice di matrici costanti.</span><span class="sxs-lookup"><span data-stu-id="e1427-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="e1427-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e1427-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1427-111">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1427-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1427-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="e1427-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="e1427-113">Matrice di puntatori a matrici non transposte.</span><span class="sxs-lookup"><span data-stu-id="e1427-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="e1427-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e1427-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1427-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e1427-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1427-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1427-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1427-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="e1427-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1427-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1427-118">Return value</span></span>

<span data-ttu-id="e1427-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1427-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1427-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1427-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e1427-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e1427-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1427-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1427-122">Remarks</span></span>

<span data-ttu-id="e1427-123">Una matrice non trasposta contiene dati di riga: principali; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="e1427-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1427-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1427-124">Requirements</span></span>



| <span data-ttu-id="e1427-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1427-125">Requirement</span></span> | <span data-ttu-id="e1427-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e1427-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1427-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1427-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e1427-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1427-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e1427-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1427-129">Library</span></span><br/> | <dl> <span data-ttu-id="e1427-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1427-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e1427-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1427-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1427-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e1427-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
