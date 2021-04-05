---
description: Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Metodo ID3DXConstantTable:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969376"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="0ec3e-103">Metodo ID3DXConstantTable:: GetConstantDesc</span><span class="sxs-lookup"><span data-stu-id="0ec3e-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="0ec3e-104">Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec3e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ec3e-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="0ec3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ec3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ec3e-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ec3e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec3e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0ec3e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0ec3e-109">Identificatore univoco di una costante.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-109">Unique identifier to a constant.</span></span> <span data-ttu-id="0ec3e-110">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0ec3e-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ec3e-111">*pDesc* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0ec3e-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec3e-112">Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ec3e-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="0ec3e-113">Restituisce un puntatore a una matrice di descrizioni.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="0ec3e-114">Vedere [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="0ec3e-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ec3e-115">*pcount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0ec3e-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec3e-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ec3e-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0ec3e-117">L'input specificato deve corrispondere alla dimensione massima della matrice.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="0ec3e-118">L'output è il numero di elementi che vengono compilati nella matrice quando la funzione restituisce.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ec3e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ec3e-119">Return value</span></span>

<span data-ttu-id="0ec3e-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ec3e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ec3e-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ec3e-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ec3e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ec3e-123">Remarks</span></span>

<span data-ttu-id="0ec3e-124">**ID3DXConstantTable:: GetConstantDesc** a volte restituisce una [**\_ Descrizione D3DXCONSTANT**](d3dxconstant-desc.md) con un \_ conteggio dei registri pari a 0.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="0ec3e-125">Questa operazione viene eseguita con una costante presente in più di un \_ set di registri, ma in tale set di registri non è allocato spazio.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="0ec3e-126">Poiché un campionatore può apparire più di una volta in una tabella costante, questo metodo può restituire una matrice di descrizioni, ognuna con un indice di registro diverso.</span><span class="sxs-lookup"><span data-stu-id="0ec3e-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec3e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ec3e-127">Requirements</span></span>



| <span data-ttu-id="0ec3e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec3e-128">Requirement</span></span> | <span data-ttu-id="0ec3e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0ec3e-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec3e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ec3e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0ec3e-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec3e-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0ec3e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ec3e-132">Library</span></span><br/> | <dl> <span data-ttu-id="0ec3e-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ec3e-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ec3e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ec3e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec3e-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0ec3e-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="0ec3e-136">**ID3DXConstantTable:: getdesc**</span><span class="sxs-lookup"><span data-stu-id="0ec3e-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
