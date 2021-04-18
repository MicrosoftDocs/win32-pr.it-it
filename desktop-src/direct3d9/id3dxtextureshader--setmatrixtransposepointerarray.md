---
description: Imposta una matrice di puntatori a matrici trasposte.
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'Metodo ID3DXTextureShader:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322782"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="42d54-103">Metodo ID3DXTextureShader:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="42d54-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="42d54-104">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="42d54-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d54-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42d54-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="42d54-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42d54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d54-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42d54-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d54-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="42d54-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="42d54-109">Identificatore univoco della matrice di costanti della matrice.</span><span class="sxs-lookup"><span data-stu-id="42d54-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="42d54-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="42d54-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="42d54-111">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42d54-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d54-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="42d54-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="42d54-113">Matrice di puntatori alle matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="42d54-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="42d54-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="42d54-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="42d54-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="42d54-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d54-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42d54-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42d54-117">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="42d54-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d54-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42d54-118">Return value</span></span>

<span data-ttu-id="42d54-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42d54-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42d54-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42d54-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42d54-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="42d54-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d54-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="42d54-122">Remarks</span></span>

<span data-ttu-id="42d54-123">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="42d54-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d54-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42d54-124">Requirements</span></span>



| <span data-ttu-id="42d54-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d54-125">Requirement</span></span> | <span data-ttu-id="42d54-126">Valore</span><span class="sxs-lookup"><span data-stu-id="42d54-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d54-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42d54-127">Header</span></span><br/>  | <dl> <span data-ttu-id="42d54-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d54-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="42d54-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="42d54-129">Library</span></span><br/> | <dl> <span data-ttu-id="42d54-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42d54-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="42d54-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42d54-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d54-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="42d54-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
