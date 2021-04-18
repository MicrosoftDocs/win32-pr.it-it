---
description: Associa un oggetto ID3DXTextureGutterHelper all'oggetto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'Metodo ID3DXPRTBuffer:: AttachGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323046"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="d3055-103">Metodo ID3DXPRTBuffer:: AttachGH</span><span class="sxs-lookup"><span data-stu-id="d3055-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="d3055-104">Associa un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d3055-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3055-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3055-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="d3055-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3055-107">*PGH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3055-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3055-108">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="d3055-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="d3055-109">Puntatore all'interfaccia [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) di un oggetto che contiene dati di rilegatura della trama.</span><span class="sxs-lookup"><span data-stu-id="d3055-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3055-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3055-110">Return value</span></span>

<span data-ttu-id="d3055-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3055-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3055-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3055-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3055-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3055-113">Remarks</span></span>

<span data-ttu-id="d3055-114">Il conteggio dei riferimenti dell'oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) verrà automaticamente incrementato di uno.</span><span class="sxs-lookup"><span data-stu-id="d3055-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="d3055-115">Verranno rilasciati tutti i puntatori **ID3DXTextureGutterHelper** esistenti.</span><span class="sxs-lookup"><span data-stu-id="d3055-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="d3055-116">È necessario assicurarsi che il numero di chiamate a **ID3DXPRTBuffer:: AttachGH** corrisponda al numero di chiamate a [**ID3DXPRTBuffer:: ReleaseGH**](id3dxprtbuffer--releasegh.md) .</span><span class="sxs-lookup"><span data-stu-id="d3055-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="d3055-117">Dopo la chiamata a **ID3DXPRTBuffer:: ReleaseGH**, il puntatore PGH restituito da **ID3DXPRTBuffer:: AttachGH** non deve più essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d3055-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3055-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3055-118">Requirements</span></span>



| <span data-ttu-id="d3055-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3055-119">Requirement</span></span> | <span data-ttu-id="d3055-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d3055-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3055-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3055-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d3055-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3055-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d3055-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3055-123">Library</span></span><br/> | <dl> <span data-ttu-id="d3055-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3055-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3055-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3055-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3055-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="d3055-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="d3055-127">**ID3DXPRTBuffer::ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="d3055-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




