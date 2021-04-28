---
description: 'Metodo ID3DXConstantTable::SetMatrixTransposePointerArray: imposta una matrice di puntatori alle matrici trasposte.'
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: Metodo ID3DXConstantTable::SetMatrixTransposePointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fefb5a0b62174499a4631f2fe8020c25a3a8efa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115039"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="a5c9e-103">Metodo ID3DXConstantTable::SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="a5c9e-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="a5c9e-104">Imposta una matrice di puntatori alle matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5c9e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="a5c9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c9e-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a5c9e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c9e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a5c9e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a5c9e-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a5c9e-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a5c9e-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c9e-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a5c9e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a5c9e-112">Identificatore univoco della matrice di costanti di matrice.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="a5c9e-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a5c9e-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5c9e-114">*ppMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a5c9e-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c9e-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="a5c9e-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="a5c9e-116">Matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="a5c9e-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a5c9e-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5c9e-118">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a5c9e-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c9e-119">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5c9e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5c9e-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c9e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5c9e-121">Return value</span></span>

<span data-ttu-id="a5c9e-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5c9e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5c9e-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a5c9e-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c9e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5c9e-125">Remarks</span></span>

<span data-ttu-id="a5c9e-126">Una matrice trasposta contiene dati principali della colonna. ciò significa che ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="a5c9e-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c9e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5c9e-127">Requirements</span></span>



| <span data-ttu-id="a5c9e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c9e-128">Requirement</span></span> | <span data-ttu-id="a5c9e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a5c9e-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c9e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5c9e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a5c9e-131"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c9e-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a5c9e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5c9e-132">Library</span></span><br/> | <dl> <span data-ttu-id="a5c9e-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5c9e-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a5c9e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5c9e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c9e-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a5c9e-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
