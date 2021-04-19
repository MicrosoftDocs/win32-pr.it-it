---
description: Imposta una matrice di vettori 4D.
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'Metodo ID3DXConstantTable:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322795"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="1f578-103">Metodo ID3DXConstantTable:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="1f578-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="1f578-104">Imposta una matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="1f578-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f578-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f578-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="1f578-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f578-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f578-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f578-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f578-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1f578-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1f578-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="1f578-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="1f578-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f578-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f578-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1f578-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1f578-112">Identificatore univoco della matrice di costanti vettoriali.</span><span class="sxs-lookup"><span data-stu-id="1f578-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="1f578-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f578-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f578-114">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f578-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f578-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f578-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f578-116">Matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="1f578-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="1f578-117">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1f578-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f578-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f578-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f578-119">Numero di vettori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1f578-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f578-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f578-120">Return value</span></span>

<span data-ttu-id="1f578-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f578-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f578-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f578-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1f578-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1f578-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f578-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f578-124">Requirements</span></span>



| <span data-ttu-id="1f578-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f578-125">Requirement</span></span> | <span data-ttu-id="1f578-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1f578-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f578-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f578-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1f578-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f578-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1f578-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f578-129">Library</span></span><br/> | <dl> <span data-ttu-id="1f578-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f578-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f578-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f578-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f578-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="1f578-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
