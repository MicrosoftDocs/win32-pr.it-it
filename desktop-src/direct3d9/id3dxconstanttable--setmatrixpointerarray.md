---
description: Imposta una matrice di puntatori alle matrici nontransposed.
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'Metodo ID3DXConstantTable:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322805"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="8745f-103">Metodo ID3DXConstantTable:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="8745f-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="8745f-104">Imposta una matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="8745f-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8745f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8745f-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="8745f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8745f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8745f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8745f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8745f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8745f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8745f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="8745f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="8745f-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8745f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8745f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8745f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8745f-112">Identificatore univoco di una matrice di matrici costanti.</span><span class="sxs-lookup"><span data-stu-id="8745f-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="8745f-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8745f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8745f-114">*ppMatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8745f-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8745f-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="8745f-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="8745f-116">Matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="8745f-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="8745f-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8745f-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8745f-118">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8745f-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8745f-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8745f-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8745f-120">Numero di matrici nella matrice.</span><span class="sxs-lookup"><span data-stu-id="8745f-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8745f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8745f-121">Return value</span></span>

<span data-ttu-id="8745f-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8745f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8745f-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8745f-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8745f-124">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8745f-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8745f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8745f-125">Remarks</span></span>

<span data-ttu-id="8745f-126">Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.</span><span class="sxs-lookup"><span data-stu-id="8745f-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="8745f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8745f-127">Requirements</span></span>



| <span data-ttu-id="8745f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8745f-128">Requirement</span></span> | <span data-ttu-id="8745f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8745f-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8745f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8745f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8745f-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8745f-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8745f-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="8745f-132">Library</span></span><br/> | <dl> <span data-ttu-id="8745f-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8745f-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8745f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8745f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8745f-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8745f-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
