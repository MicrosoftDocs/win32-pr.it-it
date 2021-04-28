---
description: 'Metodo ID3DXConstantTable::SetMatrixTransposeArray: imposta una matrice di matrici trasposte.'
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: Metodo ID3DXConstantTable::SetMatrixTransposeArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0118c888adc52671a943b7b159bae80deca26a1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115049"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="0b907-103">Metodo ID3DXConstantTable::SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="0b907-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="0b907-104">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="0b907-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b907-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b907-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="0b907-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b907-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b907-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b907-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b907-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0b907-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0b907-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="0b907-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0b907-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b907-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b907-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0b907-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0b907-112">Identificatore univoco della matrice di costanti di matrice.</span><span class="sxs-lookup"><span data-stu-id="0b907-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="0b907-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b907-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b907-114">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b907-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b907-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b907-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0b907-116">Matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="0b907-116">Array of transposed matrices.</span></span> <span data-ttu-id="0b907-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0b907-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b907-118">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b907-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b907-119">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b907-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b907-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0b907-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b907-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b907-121">Return value</span></span>

<span data-ttu-id="0b907-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b907-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b907-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b907-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b907-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b907-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b907-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b907-125">Requirements</span></span>



| <span data-ttu-id="0b907-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b907-126">Requirement</span></span> | <span data-ttu-id="0b907-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0b907-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b907-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b907-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0b907-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="0b907-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0b907-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b907-130">Library</span></span><br/> | <dl> <span data-ttu-id="0b907-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b907-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b907-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b907-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b907-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0b907-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
