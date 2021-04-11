---
description: Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice. La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Metodo ID3DXBaseMesh:: UpdateSemantics (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058621"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="a8f2b-104">Metodo ID3DXBaseMesh:: UpdateSemantics</span><span class="sxs-lookup"><span data-stu-id="a8f2b-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="a8f2b-105">Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="a8f2b-106">La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f2b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8f2b-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="a8f2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8f2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f2b-109">*Dichiarazione* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a8f2b-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f2b-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="a8f2b-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="a8f2b-111">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il formato del vertice dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="a8f2b-112">Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="a8f2b-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f2b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8f2b-113">Return value</span></span>

<span data-ttu-id="a8f2b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8f2b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8f2b-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8f2b-116">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f2b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8f2b-117">Remarks</span></span>

<span data-ttu-id="a8f2b-118">[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) viene usato per riformattare e modificare il layout dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="a8f2b-119">Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via, che non erano presenti prima.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="a8f2b-120">**ID3DXBaseMesh:: UpdateSemantics** è un metodo per l'aggiornamento della dichiarazione di vertice con informazioni semantiche diverse, senza modificare il layout del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="a8f2b-121">Ad esempio, usarlo per rietichettare una coordinata di trama 3D come binormale o tangente oppure viceversa.</span><span class="sxs-lookup"><span data-stu-id="a8f2b-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f2b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8f2b-122">Requirements</span></span>



| <span data-ttu-id="a8f2b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f2b-123">Requirement</span></span> | <span data-ttu-id="a8f2b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a8f2b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f2b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8f2b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a8f2b-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f2b-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a8f2b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8f2b-127">Library</span></span><br/> | <dl> <span data-ttu-id="a8f2b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8f2b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8f2b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8f2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f2b-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a8f2b-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="a8f2b-131">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="a8f2b-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="a8f2b-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="a8f2b-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
