---
description: Crea un oggetto mesh usando un dichiaratore.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Funzione D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323274"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="8d9b5-103">D3DX10CreateMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="8d9b5-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="8d9b5-104">Crea un oggetto mesh usando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d9b5-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8d9b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d9b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9b5-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="8d9b5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="8d9b5-109">Puntatore a un' [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), l'oggetto dispositivo da associare alla mesh.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-110">*pDeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-111">Tipo: **const [**D3D10 \_ input \_ elemento \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8d9b5-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="8d9b5-112">Matrice di [**elementi \_ \_ \_ desc dell'elemento input D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , che descrive il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="8d9b5-113">Questo parametro deve essere mappato direttamente a un FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="8d9b5-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-114">*DeclCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9b5-116">Numero di elementi in pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-117">*pPositionSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9b5-119">Semantica che identifica la parte della dichiarazione del vertice contenente le informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-120">*VertexCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9b5-122">Numero di vertici per la mesh.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="8d9b5-123">Questo parametro deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-124">*FaceCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9b5-126">Numero di visi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-126">Number of faces for the mesh.</span></span> <span data-ttu-id="8d9b5-127">L'intervallo valido per questo numero è maggiore di 0 e uno minore del valore DWORD massimo (in genere 65534), perché l'ultimo indice è riservato.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-128">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d9b5-130">Combinazione di uno o più flag dalla [**\_ mesh d3dx10**](d3dx10-mesh.md), specificando le opzioni per la mesh.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d9b5-131">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8d9b5-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9b5-132">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8d9b5-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="8d9b5-133">Indirizzo di un puntatore a un' [**interfaccia ID3DX10Mesh**](id3dx10mesh.md), che rappresenta l'oggetto mesh creato.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9b5-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d9b5-134">Return value</span></span>

<span data-ttu-id="8d9b5-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d9b5-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d9b5-136">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d9b5-137">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8d9b5-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9b5-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d9b5-138">Requirements</span></span>



| <span data-ttu-id="8d9b5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9b5-139">Requirement</span></span> | <span data-ttu-id="8d9b5-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8d9b5-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9b5-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d9b5-141">Header</span></span><br/>  | <dl> <span data-ttu-id="8d9b5-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9b5-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8d9b5-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d9b5-143">Library</span></span><br/> | <dl> <span data-ttu-id="8d9b5-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9b5-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d9b5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d9b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9b5-146">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8d9b5-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="8d9b5-147">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="8d9b5-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
