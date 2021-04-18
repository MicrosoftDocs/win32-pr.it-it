---
description: Crea una nuova mesh e la riempie con i dati di una mesh precedentemente caricata.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Metodo ID3DX10Mesh:: CloneMesh (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323161"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="8fe99-103">Metodo ID3DX10Mesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="8fe99-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="8fe99-104">Crea una nuova mesh e la riempie con i dati di una mesh precedentemente caricata.</span><span class="sxs-lookup"><span data-stu-id="8fe99-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fe99-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8fe99-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fe99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe99-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe99-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe99-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe99-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe99-109">Flag di creazione da applicare alla nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="8fe99-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="8fe99-110">Vedere [**d3dx10 \_ mesh**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="8fe99-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fe99-111">*pPosSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe99-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe99-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe99-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe99-113">Nome semantico per i dati di posizione.</span><span class="sxs-lookup"><span data-stu-id="8fe99-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="8fe99-114">*pDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe99-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe99-115">Tipo: **const [**D3D10 \_ input \_ elemento \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8fe99-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="8fe99-116">Matrice di \_ \_ strutture desc dell'elemento input D3D10, che \_ descrive il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="8fe99-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="8fe99-117">Vedere [**l' \_ elemento di input D3D10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="8fe99-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="8fe99-118">*DeclCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe99-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe99-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe99-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe99-120">Numero di elementi nella matrice pDesc.</span><span class="sxs-lookup"><span data-stu-id="8fe99-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="8fe99-121">*ppCloneMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8fe99-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe99-122">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8fe99-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="8fe99-123">Nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="8fe99-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe99-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fe99-124">Return value</span></span>

<span data-ttu-id="8fe99-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fe99-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fe99-126">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8fe99-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe99-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fe99-127">Requirements</span></span>



| <span data-ttu-id="8fe99-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe99-128">Requirement</span></span> | <span data-ttu-id="8fe99-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8fe99-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe99-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fe99-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8fe99-131"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe99-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fe99-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fe99-132">Library</span></span><br/> | <dl> <span data-ttu-id="8fe99-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fe99-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe99-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fe99-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe99-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8fe99-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8fe99-136">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="8fe99-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
