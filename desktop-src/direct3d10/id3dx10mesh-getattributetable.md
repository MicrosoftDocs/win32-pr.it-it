---
description: Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'Metodo ID3DX10Mesh:: GetAttributeTable (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323150"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="04bc2-103">Metodo ID3DX10Mesh:: GetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="04bc2-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="04bc2-104">Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.</span><span class="sxs-lookup"><span data-stu-id="04bc2-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="04bc2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04bc2-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="04bc2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04bc2-107">*pAttribTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04bc2-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04bc2-108">Tipo: **[ **\_ \_ intervallo di attributi di d3dx10**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="04bc2-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="04bc2-109">Puntatore a una matrice di \_ strutture di intervalli di attributi d3dx10 \_ , che rappresenta le voci nella tabella degli attributi della mesh.</span><span class="sxs-lookup"><span data-stu-id="04bc2-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="04bc2-110">Specificare **null** per recuperare il valore per pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="04bc2-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="04bc2-111">*pAttribTableSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04bc2-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04bc2-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04bc2-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04bc2-113">Puntatore al numero di voci archiviate in pAttribTable o a un valore da compilare con il numero di voci archiviate nella tabella degli attributi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="04bc2-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04bc2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04bc2-114">Return value</span></span>

<span data-ttu-id="04bc2-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04bc2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04bc2-116">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="04bc2-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04bc2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="04bc2-117">Remarks</span></span>

<span data-ttu-id="04bc2-118">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="04bc2-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="04bc2-119">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="04bc2-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="04bc2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04bc2-120">Requirements</span></span>



| <span data-ttu-id="04bc2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bc2-121">Requirement</span></span> | <span data-ttu-id="04bc2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="04bc2-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04bc2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04bc2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04bc2-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="04bc2-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="04bc2-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="04bc2-125">Library</span></span><br/> | <dl> <span data-ttu-id="04bc2-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04bc2-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04bc2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04bc2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bc2-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="04bc2-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="04bc2-129">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="04bc2-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
