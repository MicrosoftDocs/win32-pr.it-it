---
description: Converte il subset di mesh specificato in una serie di strisce.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Funzione D3DXConvertMeshSubsetToStrips (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323424"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="3aa37-103">D3DXConvertMeshSubsetToStrips (funzione)</span><span class="sxs-lookup"><span data-stu-id="3aa37-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="3aa37-104">Converte il subset di mesh specificato in una serie di strisce.</span><span class="sxs-lookup"><span data-stu-id="3aa37-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3aa37-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="3aa37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aa37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa37-107">*Meshin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa37-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="3aa37-109">Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta la mesh da convertire in una striscia.</span><span class="sxs-lookup"><span data-stu-id="3aa37-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-110">*AttribId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa37-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa37-112">ID dell'attributo del sottoinsieme mesh da convertire in strip.</span><span class="sxs-lookup"><span data-stu-id="3aa37-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-113">*IBOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa37-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa37-115">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specificano le opzioni per la creazione del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3aa37-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="3aa37-116">Non può essere D3DXMESH a \_ 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3aa37-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="3aa37-117">Il buffer dell'indice verrà creato con indici a 32 bit o a 16 bit a seconda del formato del buffer dell'indice della mesh specificata dal parametro *meshin* .</span><span class="sxs-lookup"><span data-stu-id="3aa37-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-118">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="3aa37-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="3aa37-120">Puntatore a un'interfaccia [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , che rappresenta il buffer di indice contenente la striscia.</span><span class="sxs-lookup"><span data-stu-id="3aa37-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-121">*pNumIndices* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3aa37-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3aa37-123">Numero di indici nel buffer restituito nel parametro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="3aa37-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-124">*ppStripLengths* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3aa37-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3aa37-126">Buffer contenente una matrice di un DWORD per striscia, che specifica il numero di triangoli nell'oggetto Strip.</span><span class="sxs-lookup"><span data-stu-id="3aa37-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-127">*pNumStrips* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3aa37-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3aa37-129">Numero di singole strisce nel buffer di indice e nella matrice di lunghezza della striscia corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3aa37-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa37-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aa37-130">Return value</span></span>

<span data-ttu-id="3aa37-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3aa37-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3aa37-132">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3aa37-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3aa37-133">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="3aa37-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa37-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="3aa37-134">Remarks</span></span>

<span data-ttu-id="3aa37-135">Prima di eseguire questa funzione, chiamare [**optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con il \_ flag D3DXMESHOPT ATTRSORT impostato.</span><span class="sxs-lookup"><span data-stu-id="3aa37-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa37-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aa37-136">Requirements</span></span>



| <span data-ttu-id="3aa37-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa37-137">Requirement</span></span> | <span data-ttu-id="3aa37-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3aa37-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa37-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3aa37-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa37-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa37-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3aa37-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="3aa37-141">Library</span></span><br/> | <dl> <span data-ttu-id="3aa37-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aa37-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3aa37-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aa37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa37-144">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="3aa37-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
