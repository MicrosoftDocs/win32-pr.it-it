---
description: Imposta una matrice di matrici trasposte.
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'Metodo ID3DXConstantTable:: SetMatrixTransposeArray (D3DX9Shader. h)'
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
ms.openlocfilehash: 69755ed973a8c412373287f128642b78ea2ad346
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530943"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="7c80f-103">Metodo ID3DXConstantTable:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="7c80f-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="7c80f-104">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="7c80f-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c80f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c80f-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7c80f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c80f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c80f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c80f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c80f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7c80f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7c80f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="7c80f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7c80f-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c80f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c80f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c80f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c80f-112">Identificatore univoco della matrice di costanti della matrice.</span><span class="sxs-lookup"><span data-stu-id="7c80f-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="7c80f-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c80f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c80f-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c80f-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c80f-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c80f-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c80f-116">Matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="7c80f-116">Array of transposed matrices.</span></span> <span data-ttu-id="7c80f-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7c80f-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c80f-118">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7c80f-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c80f-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c80f-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c80f-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7c80f-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c80f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c80f-121">Return value</span></span>

<span data-ttu-id="7c80f-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c80f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c80f-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c80f-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c80f-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7c80f-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c80f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c80f-125">Requirements</span></span>



| <span data-ttu-id="7c80f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c80f-126">Requirement</span></span> | <span data-ttu-id="7c80f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7c80f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c80f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c80f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7c80f-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c80f-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7c80f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c80f-130">Library</span></span><br/> | <dl> <span data-ttu-id="7c80f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c80f-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c80f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c80f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c80f-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7c80f-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
