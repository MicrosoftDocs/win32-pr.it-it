---
description: Allocare spazio per altri vertici.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'Metodo ID3DX10SkinInfo:: AddVertices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323676"
---
# <a name="id3dx10skininfoaddvertices-method"></a><span data-ttu-id="53dda-103">Metodo ID3DX10SkinInfo:: AddVertices</span><span class="sxs-lookup"><span data-stu-id="53dda-103">ID3DX10SkinInfo::AddVertices method</span></span>

<span data-ttu-id="53dda-104">Allocare spazio per altri vertici.</span><span class="sxs-lookup"><span data-stu-id="53dda-104">Allocate space for additional vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="53dda-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53dda-105">Syntax</span></span>


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="53dda-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53dda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53dda-107">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="53dda-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53dda-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53dda-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53dda-109">Numero di vertici da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="53dda-109">The number of vertices to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53dda-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53dda-110">Return value</span></span>

<span data-ttu-id="53dda-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53dda-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53dda-112">Se questo metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53dda-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="53dda-113">Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="53dda-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="53dda-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53dda-114">Requirements</span></span>



| <span data-ttu-id="53dda-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53dda-115">Requirement</span></span> | <span data-ttu-id="53dda-116">Valore</span><span class="sxs-lookup"><span data-stu-id="53dda-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53dda-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53dda-117">Header</span></span><br/>  | <dl> <span data-ttu-id="53dda-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="53dda-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="53dda-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="53dda-119">Library</span></span><br/> | <dl> <span data-ttu-id="53dda-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53dda-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53dda-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53dda-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53dda-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="53dda-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="53dda-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="53dda-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
