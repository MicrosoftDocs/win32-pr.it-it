---
description: Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'Metodo ID3DXTextureShader:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323358"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="a81c7-103">Metodo ID3DXTextureShader:: GetConstantDesc</span><span class="sxs-lookup"><span data-stu-id="a81c7-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="a81c7-104">Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="a81c7-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a81c7-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="a81c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a81c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a81c7-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a81c7-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a81c7-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a81c7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a81c7-109">Identificatore univoco di una costante.</span><span class="sxs-lookup"><span data-stu-id="a81c7-109">Unique identifier to a constant.</span></span> <span data-ttu-id="a81c7-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a81c7-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a81c7-111">*pDesc* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a81c7-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a81c7-112">Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a81c7-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="a81c7-113">Restituisce un puntatore a una matrice di descrizioni.</span><span class="sxs-lookup"><span data-stu-id="a81c7-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="a81c7-114">Vedere [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="a81c7-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="a81c7-115">*pcount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a81c7-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a81c7-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a81c7-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a81c7-117">L'input specificato deve corrispondere alla dimensione massima della matrice.</span><span class="sxs-lookup"><span data-stu-id="a81c7-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="a81c7-118">L'output è il numero di elementi che vengono compilati nella matrice quando la funzione restituisce.</span><span class="sxs-lookup"><span data-stu-id="a81c7-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a81c7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a81c7-119">Return value</span></span>

<span data-ttu-id="a81c7-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a81c7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a81c7-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a81c7-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a81c7-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a81c7-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a81c7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a81c7-123">Remarks</span></span>

<span data-ttu-id="a81c7-124">I sampler possono essere visualizzati più di una volta in una tabella costante, pertanto questo metodo può restituire una matrice di descrizioni ognuna con un indice di registro diverso.</span><span class="sxs-lookup"><span data-stu-id="a81c7-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a81c7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a81c7-125">Requirements</span></span>



| <span data-ttu-id="a81c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a81c7-126">Requirement</span></span> | <span data-ttu-id="a81c7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a81c7-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a81c7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a81c7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a81c7-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a81c7-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a81c7-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="a81c7-130">Library</span></span><br/> | <dl> <span data-ttu-id="a81c7-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a81c7-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a81c7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a81c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a81c7-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a81c7-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="a81c7-134">**ID3DXTextureShader:: getdesc**</span><span class="sxs-lookup"><span data-stu-id="a81c7-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
