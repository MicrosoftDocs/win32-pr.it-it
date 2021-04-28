---
description: "Funzione D3DX10CreateSkinInfo: crea un oggetto mesh dell'interfaccia vuota usando un dichiaratore."
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Funzione D3DX10CreateSkinInfo (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103599"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="0e344-103">Funzione D3DX10CreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="0e344-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="0e344-104">Crea un oggetto mesh dell'interfaccia vuota usando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="0e344-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e344-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e344-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0e344-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e344-107">*ppSkinInfo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0e344-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e344-108">Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e344-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="0e344-109">Indirizzo di un puntatore a [**un'interfaccia ID3DX10SkinInfo**](id3dx10skininfo.md)che rappresenta l'oggetto mesh dell'interfaccia creata.</span><span class="sxs-lookup"><span data-stu-id="0e344-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e344-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e344-110">Return value</span></span>

<span data-ttu-id="0e344-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e344-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e344-112">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e344-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e344-113">Se la funzione ha esito negativo, il valore restituito può essere E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0e344-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e344-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e344-114">Remarks</span></span>

<span data-ttu-id="0e344-115">Usare [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) per popolare l'oggetto mesh dell'interfaccia vuota restituito da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0e344-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e344-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e344-116">Requirements</span></span>



| <span data-ttu-id="0e344-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e344-117">Requirement</span></span> | <span data-ttu-id="0e344-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0e344-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e344-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e344-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e344-120"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="0e344-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0e344-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e344-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e344-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e344-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e344-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e344-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e344-124">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="0e344-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="0e344-125">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="0e344-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




