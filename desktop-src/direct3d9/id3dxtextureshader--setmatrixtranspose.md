---
description: Imposta una matrice trasposta.
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'Metodo ID3DXTextureShader:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf5507d935d2fea1b6210624e70344a2c4a1da81
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969372"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="6787e-103">Metodo ID3DXTextureShader:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="6787e-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="6787e-104">Imposta una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="6787e-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6787e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6787e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="6787e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6787e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6787e-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6787e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6787e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6787e-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="6787e-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="6787e-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="6787e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="6787e-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6787e-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787e-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6787e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6787e-113">Puntatore a una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="6787e-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="6787e-114">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="6787e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6787e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6787e-115">Return value</span></span>

<span data-ttu-id="6787e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6787e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6787e-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6787e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6787e-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6787e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6787e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6787e-119">Remarks</span></span>

<span data-ttu-id="6787e-120">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="6787e-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="6787e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6787e-121">Requirements</span></span>



| <span data-ttu-id="6787e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6787e-122">Requirement</span></span> | <span data-ttu-id="6787e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6787e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6787e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6787e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6787e-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6787e-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6787e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6787e-126">Library</span></span><br/> | <dl> <span data-ttu-id="6787e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6787e-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6787e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6787e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6787e-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="6787e-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




