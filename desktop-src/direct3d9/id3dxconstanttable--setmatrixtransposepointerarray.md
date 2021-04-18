---
description: Imposta una matrice di puntatori a matrici trasposte.
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'Metodo ID3DXConstantTable:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
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
ms.openlocfilehash: 6c78c051ff2d2ab52c9a741fa117a89f66ff450d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322800"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="bcebd-103">Metodo ID3DXConstantTable:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="bcebd-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="bcebd-104">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="bcebd-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcebd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcebd-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="bcebd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcebd-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcebd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcebd-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bcebd-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bcebd-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="bcebd-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="bcebd-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcebd-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcebd-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bcebd-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bcebd-112">Identificatore univoco della matrice di costanti della matrice.</span><span class="sxs-lookup"><span data-stu-id="bcebd-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="bcebd-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bcebd-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcebd-114">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcebd-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcebd-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="bcebd-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="bcebd-116">Matrice di puntatori alle matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="bcebd-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="bcebd-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="bcebd-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcebd-118">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bcebd-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcebd-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bcebd-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bcebd-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="bcebd-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcebd-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcebd-121">Return value</span></span>

<span data-ttu-id="bcebd-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bcebd-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bcebd-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bcebd-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bcebd-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bcebd-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcebd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcebd-125">Remarks</span></span>

<span data-ttu-id="bcebd-126">Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.</span><span class="sxs-lookup"><span data-stu-id="bcebd-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcebd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcebd-127">Requirements</span></span>



| <span data-ttu-id="bcebd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcebd-128">Requirement</span></span> | <span data-ttu-id="bcebd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bcebd-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcebd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcebd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bcebd-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcebd-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bcebd-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="bcebd-132">Library</span></span><br/> | <dl> <span data-ttu-id="bcebd-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcebd-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bcebd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcebd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcebd-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="bcebd-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
