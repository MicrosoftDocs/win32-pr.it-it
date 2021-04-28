---
description: 'Funzione D3DX10CreateMesh: crea un oggetto mesh usando un dichiaratore.'
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Funzione D3DX10CreateMesh (D3DX10Mesh.h)
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
ms.openlocfilehash: cc744536336a4a102bafeaeae3ba87bbad58eb97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113359"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="2072e-103">Funzione D3DX10CreateMesh</span><span class="sxs-lookup"><span data-stu-id="2072e-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="2072e-104">Crea un oggetto mesh usando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="2072e-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="2072e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2072e-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2072e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2072e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2072e-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="2072e-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="2072e-109">Puntatore a [**un'interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), l'oggetto dispositivo da associare alla mesh.</span><span class="sxs-lookup"><span data-stu-id="2072e-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-110">*pDeclaration* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-111">Tipo: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2072e-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="2072e-112">Matrice di [**elementi D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) che descrivono il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="2072e-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="2072e-113">Questo parametro deve essere mappato direttamente a un formato FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="2072e-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="2072e-114">*DeclCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2072e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2072e-116">Numero di elementi in pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="2072e-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-117">*pPositionSemantic* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2072e-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2072e-119">Semantica che identifica la parte della dichiarazione del vertice che contiene informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="2072e-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-120">*VertexCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-121">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2072e-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2072e-122">Numero di vertici per la mesh.</span><span class="sxs-lookup"><span data-stu-id="2072e-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="2072e-123">Questo parametro deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="2072e-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-124">*FaceCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-125">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2072e-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2072e-126">Numero di visi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="2072e-126">Number of faces for the mesh.</span></span> <span data-ttu-id="2072e-127">L'intervallo valido per questo numero è maggiore di 0 e uno minore del valore DWORD massimo (in genere 65534), perché l'ultimo indice è riservato.</span><span class="sxs-lookup"><span data-stu-id="2072e-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-128">*Opzioni* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2072e-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-129">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2072e-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2072e-130">Combinazione di uno o più flag da [**D3DX10 \_ MESH,**](d3dx10-mesh.md)specificando le opzioni per la mesh.</span><span class="sxs-lookup"><span data-stu-id="2072e-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2072e-131">*ppMesh* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="2072e-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2072e-132">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2072e-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="2072e-133">Indirizzo di un puntatore a [**un'interfaccia ID3DX10Mesh**](id3dx10mesh.md)che rappresenta l'oggetto mesh creato.</span><span class="sxs-lookup"><span data-stu-id="2072e-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2072e-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2072e-134">Return value</span></span>

<span data-ttu-id="2072e-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2072e-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2072e-136">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2072e-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2072e-137">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2072e-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2072e-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2072e-138">Requirements</span></span>



| <span data-ttu-id="2072e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2072e-139">Requirement</span></span> | <span data-ttu-id="2072e-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2072e-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2072e-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2072e-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2072e-142"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="2072e-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2072e-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="2072e-143">Library</span></span><br/> | <dl> <span data-ttu-id="2072e-144"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2072e-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2072e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2072e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2072e-146">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="2072e-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="2072e-147">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="2072e-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
