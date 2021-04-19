---
description: Annullare un buffer.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'Metodo ID3DX10MeshBuffer:: annullare (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323763"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="1d6fd-103">Metodo ID3DX10MeshBuffer:: annullare</span><span class="sxs-lookup"><span data-stu-id="1d6fd-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="1d6fd-104">Annullare un buffer.</span><span class="sxs-lookup"><span data-stu-id="1d6fd-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d6fd-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="1d6fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d6fd-106">Parameters</span></span>

<span data-ttu-id="1d6fd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1d6fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d6fd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d6fd-108">Return value</span></span>

<span data-ttu-id="1d6fd-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d6fd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d6fd-110">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1d6fd-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d6fd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d6fd-111">Remarks</span></span>



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6fd-112">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="1d6fd-112">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="1d6fd-113">Annullare () in Direct3D 10 è analogo allo sblocco di risorse () in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="1d6fd-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1d6fd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d6fd-114">Requirements</span></span>



| <span data-ttu-id="1d6fd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d6fd-115">Requirement</span></span> | <span data-ttu-id="1d6fd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1d6fd-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6fd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d6fd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1d6fd-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d6fd-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d6fd-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d6fd-119">Library</span></span><br/> | <dl> <span data-ttu-id="1d6fd-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d6fd-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6fd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d6fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6fd-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="1d6fd-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="1d6fd-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1d6fd-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




