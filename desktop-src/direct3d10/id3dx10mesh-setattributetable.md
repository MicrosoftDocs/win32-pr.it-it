---
description: 'Metodo ID3DX10Mesh::SetAttributeTable: imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: Metodo ID3DX10Mesh::SetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084009"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="463d2-103">Metodo ID3DX10Mesh::SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="463d2-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="463d2-104">Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.</span><span class="sxs-lookup"><span data-stu-id="463d2-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="463d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="463d2-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="463d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="463d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463d2-107">*pAttribTable* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="463d2-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463d2-108">Tipo: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="463d2-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="463d2-109">Puntatore a una matrice di strutture ATTRIBUTE RANGE D3DX10, che rappresenta le voci \_ nella tabella degli attributi \_ mesh.</span><span class="sxs-lookup"><span data-stu-id="463d2-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="463d2-110">*cAttribTableSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="463d2-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463d2-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463d2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="463d2-112">Numero di attributi nella tabella degli attributi della mesh.</span><span class="sxs-lookup"><span data-stu-id="463d2-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="463d2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="463d2-113">Return value</span></span>

<span data-ttu-id="463d2-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="463d2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="463d2-115">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="463d2-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="463d2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="463d2-116">Remarks</span></span>

<span data-ttu-id="463d2-117">Se un'applicazione tiene traccia delle informazioni in una tabella di attributi e riorganizza la tabella in seguito a modifiche agli attributi o ai visi, questo metodo consente all'applicazione di aggiornare le tabelle degli attributi anziché chiamare nuovamente ID3DX10Mesh::Optimize.</span><span class="sxs-lookup"><span data-stu-id="463d2-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="463d2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="463d2-118">Requirements</span></span>



| <span data-ttu-id="463d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="463d2-119">Requirement</span></span> | <span data-ttu-id="463d2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="463d2-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="463d2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="463d2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="463d2-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="463d2-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="463d2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="463d2-123">Library</span></span><br/> | <dl> <span data-ttu-id="463d2-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="463d2-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463d2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="463d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463d2-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="463d2-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="463d2-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="463d2-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
