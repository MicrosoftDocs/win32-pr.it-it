---
description: Converte il subset di mesh specificato in un singolo Strip di triangolo.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Funzione D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322448"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="5d4f8-103">D3DXConvertMeshSubsetToSingleStrip (funzione)</span><span class="sxs-lookup"><span data-stu-id="5d4f8-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="5d4f8-104">Converte il subset di mesh specificato in un singolo Strip di triangolo.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d4f8-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="5d4f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d4f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4f8-107">*Meshin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d4f8-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f8-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4f8-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="5d4f8-109">Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta la mesh da convertire in una striscia.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f8-110">*AttribId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d4f8-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f8-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4f8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4f8-112">ID dell'attributo del sottoinsieme mesh da convertire in strip.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f8-113">*IBOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d4f8-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f8-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4f8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d4f8-115">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specificano le opzioni per la creazione del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="5d4f8-116">Non può essere D3DXMESH a \_ 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="5d4f8-117">Il buffer dell'indice verrà creato con indici a 32 bit o a 16 bit, a seconda del formato del buffer dell'indice della mesh specificata dal parametro *meshin* .</span><span class="sxs-lookup"><span data-stu-id="5d4f8-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f8-118">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5d4f8-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f8-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="5d4f8-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="5d4f8-120">Puntatore a un'interfaccia [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , che rappresenta il buffer di indice contenente la striscia.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f8-121">*pNumIndices* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5d4f8-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f8-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d4f8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d4f8-123">Numero di indici nel buffer restituito nel parametro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="5d4f8-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4f8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d4f8-124">Return value</span></span>

<span data-ttu-id="5d4f8-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d4f8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d4f8-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5d4f8-127">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4f8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d4f8-128">Remarks</span></span>

<span data-ttu-id="5d4f8-129">Prima di eseguire questa funzione, chiamare [**optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con il \_ flag D3DXMESHOPT ATTRSORT impostato.</span><span class="sxs-lookup"><span data-stu-id="5d4f8-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4f8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d4f8-130">Requirements</span></span>



| <span data-ttu-id="5d4f8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d4f8-131">Requirement</span></span> | <span data-ttu-id="5d4f8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5d4f8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4f8-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d4f8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5d4f8-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4f8-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5d4f8-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d4f8-135">Library</span></span><br/> | <dl> <span data-ttu-id="5d4f8-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d4f8-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d4f8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d4f8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4f8-138">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="5d4f8-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
