---
description: Ottiene il buffer di dati che archivia i dati di animazione del fotogramma chiave compressi.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'Metodo ID3DXCompressedAnimationSet:: GetCompressedData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322838"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="6dad8-103">Metodo ID3DXCompressedAnimationSet:: GetCompressedData</span><span class="sxs-lookup"><span data-stu-id="6dad8-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="6dad8-104">Ottiene il buffer di dati che archivia i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="6dad8-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dad8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dad8-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="6dad8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dad8-107">*ppCompressedData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6dad8-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dad8-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dad8-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6dad8-109">Indirizzo di un puntatore al buffer di dati [**ID3DXBuffer**](id3dxbuffer.md) che riceve i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="6dad8-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dad8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dad8-110">Return value</span></span>

<span data-ttu-id="6dad8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6dad8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6dad8-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6dad8-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6dad8-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6dad8-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dad8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dad8-114">Requirements</span></span>



| <span data-ttu-id="6dad8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dad8-115">Requirement</span></span> | <span data-ttu-id="6dad8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6dad8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dad8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6dad8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6dad8-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dad8-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6dad8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="6dad8-119">Library</span></span><br/> | <dl> <span data-ttu-id="6dad8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dad8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6dad8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dad8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dad8-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="6dad8-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




