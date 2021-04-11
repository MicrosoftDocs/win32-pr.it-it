---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente una teiera.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Funzione D3DXCreateTeapot (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235027"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="780ad-103">D3DXCreateTeapot (funzione)</span><span class="sxs-lookup"><span data-stu-id="780ad-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="780ad-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente una teiera.</span><span class="sxs-lookup"><span data-stu-id="780ad-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="780ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="780ad-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="780ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="780ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780ad-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="780ad-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="780ad-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="780ad-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="780ad-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh teiera creata.</span><span class="sxs-lookup"><span data-stu-id="780ad-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="780ad-110">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="780ad-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="780ad-111">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="780ad-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="780ad-112">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="780ad-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="780ad-113">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="780ad-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="780ad-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="780ad-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="780ad-115">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="780ad-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="780ad-116">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="780ad-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="780ad-117">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="780ad-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780ad-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="780ad-118">Return value</span></span>

<span data-ttu-id="780ad-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="780ad-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="780ad-120">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="780ad-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="780ad-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="780ad-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="780ad-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="780ad-122">Remarks</span></span>

<span data-ttu-id="780ad-123">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="780ad-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="780ad-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="780ad-124">Requirements</span></span>



| <span data-ttu-id="780ad-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="780ad-125">Requirement</span></span> | <span data-ttu-id="780ad-126">Valore</span><span class="sxs-lookup"><span data-stu-id="780ad-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="780ad-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="780ad-127">Header</span></span><br/>  | <dl> <span data-ttu-id="780ad-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="780ad-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="780ad-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="780ad-129">Library</span></span><br/> | <dl> <span data-ttu-id="780ad-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="780ad-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="780ad-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="780ad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780ad-132">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="780ad-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
