---
description: Annulla l'associazione di un oggetto ID3DXTextureGutterHelper associato all'oggetto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Metodo ID3DXPRTBuffer:: ReleaseGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402028"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="b358d-103">Metodo ID3DXPRTBuffer:: ReleaseGH</span><span class="sxs-lookup"><span data-stu-id="b358d-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="b358d-104">Annulla l'associazione di un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) associato all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b358d-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b358d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b358d-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="b358d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b358d-106">Parameters</span></span>

<span data-ttu-id="b358d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b358d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b358d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b358d-108">Return value</span></span>

<span data-ttu-id="b358d-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b358d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b358d-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b358d-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b358d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b358d-111">Remarks</span></span>

<span data-ttu-id="b358d-112">Questo metodo rilascia il puntatore all'interfaccia [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="b358d-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="b358d-113">È necessario assicurarsi che il numero di chiamate a [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) corrisponda al numero di chiamate a **ID3DXPRTBuffer:: ReleaseGH** .</span><span class="sxs-lookup"><span data-stu-id="b358d-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="b358d-114">Dopo la chiamata a **ID3DXPRTBuffer:: ReleaseGH**, il puntatore PGH restituito da **ID3DXPRTBuffer:: AttachGH** non deve più essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b358d-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b358d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b358d-115">Requirements</span></span>



| <span data-ttu-id="b358d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b358d-116">Requirement</span></span> | <span data-ttu-id="b358d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b358d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b358d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b358d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b358d-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b358d-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b358d-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b358d-120">Library</span></span><br/> | <dl> <span data-ttu-id="b358d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b358d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b358d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b358d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b358d-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="b358d-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="b358d-124">**ID3DXPRTBuffer::AttachGH**</span><span class="sxs-lookup"><span data-stu-id="b358d-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




