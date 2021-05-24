---
description: Annullare il mapping di un buffer.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: Metodo ID3DX10MeshBuffer::Unmap (D3DX10.h)
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
ms.openlocfilehash: 11b15f8bc1e4103503b183672ebd31e92b4daea7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335375"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="5fb4f-103">Metodo ID3DX10MeshBuffer::Unmap</span><span class="sxs-lookup"><span data-stu-id="5fb4f-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="5fb4f-104">Annullare il mapping di un buffer.</span><span class="sxs-lookup"><span data-stu-id="5fb4f-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fb4f-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="5fb4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fb4f-106">Parameters</span></span>

<span data-ttu-id="5fb4f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5fb4f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fb4f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fb4f-108">Return value</span></span>

<span data-ttu-id="5fb4f-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fb4f-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fb4f-110">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="5fb4f-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb4f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fb4f-111">Remarks</span></span>



<span data-ttu-id="5fb4f-112">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="5fb4f-112">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="5fb4f-113">Unmap() in Direct3D 10 è analogo alla risorsa Unlock() in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="5fb4f-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="5fb4f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fb4f-114">Requirements</span></span>



| <span data-ttu-id="5fb4f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fb4f-115">Requirement</span></span> | <span data-ttu-id="5fb4f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5fb4f-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb4f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fb4f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5fb4f-118"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5fb4f-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5fb4f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fb4f-119">Library</span></span><br/> | <dl> <span data-ttu-id="5fb4f-120"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fb4f-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb4f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fb4f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb4f-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="5fb4f-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="5fb4f-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="5fb4f-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




