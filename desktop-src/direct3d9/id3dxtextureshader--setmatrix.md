---
description: 'Metodo ID3DXTextureShader::SetMatrix: imposta una matrice non trasposta.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: Metodo ID3DXTextureShader::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090219"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="44245-103">Metodo ID3DXTextureShader::SetMatrix</span><span class="sxs-lookup"><span data-stu-id="44245-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="44245-104">Imposta una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="44245-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="44245-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44245-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="44245-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44245-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="44245-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44245-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="44245-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="44245-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="44245-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="44245-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="44245-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="44245-111">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="44245-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44245-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="44245-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="44245-113">Puntatore a una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="44245-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="44245-114">Vedere [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="44245-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44245-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44245-115">Return value</span></span>

<span data-ttu-id="44245-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44245-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44245-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44245-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="44245-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="44245-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="44245-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="44245-119">Remarks</span></span>

<span data-ttu-id="44245-120">Una matrice non trasposta contiene dati principali della riga. ciò significa che ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="44245-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="44245-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44245-121">Requirements</span></span>



| <span data-ttu-id="44245-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="44245-122">Requirement</span></span> | <span data-ttu-id="44245-123">Valore</span><span class="sxs-lookup"><span data-stu-id="44245-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44245-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44245-124">Header</span></span><br/>  | <dl> <span data-ttu-id="44245-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="44245-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="44245-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="44245-126">Library</span></span><br/> | <dl> <span data-ttu-id="44245-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="44245-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="44245-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44245-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44245-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="44245-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




