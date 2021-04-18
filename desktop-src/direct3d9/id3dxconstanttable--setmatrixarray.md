---
description: Imposta una matrice di matrici nontransposed.
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: 'Metodo ID3DXConstantTable:: SetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 48dd85975ac58dd26d4194584ce5fbebe26da2a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322809"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="7485f-103">Metodo ID3DXConstantTable:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="7485f-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="7485f-104">Imposta una matrice di matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7485f-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7485f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7485f-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7485f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7485f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7485f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7485f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7485f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7485f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7485f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="7485f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7485f-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7485f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7485f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7485f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7485f-112">Identificatore univoco della matrice di matrici costanti.</span><span class="sxs-lookup"><span data-stu-id="7485f-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="7485f-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7485f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7485f-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7485f-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7485f-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7485f-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7485f-116">Matrice di matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7485f-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="7485f-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7485f-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7485f-118">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7485f-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7485f-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7485f-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7485f-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7485f-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7485f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7485f-121">Return value</span></span>

<span data-ttu-id="7485f-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7485f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7485f-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7485f-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7485f-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7485f-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7485f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7485f-125">Requirements</span></span>



| <span data-ttu-id="7485f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7485f-126">Requirement</span></span> | <span data-ttu-id="7485f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7485f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7485f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7485f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7485f-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7485f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="7485f-130">Library</span></span><br/> | <dl> <span data-ttu-id="7485f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7485f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7485f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7485f-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7485f-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
