---
description: 'Chiama ID3DXSprite:: Flush e ripristina lo stato del dispositivo in modo che sia stato prima della chiamata a ID3DXSprite:: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'Metodo ID3DXSprite:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401991"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="74610-103">Metodo ID3DXSprite:: end</span><span class="sxs-lookup"><span data-stu-id="74610-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="74610-104">Chiama [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) e ripristina lo stato del dispositivo in modo che sia stato prima della chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="74610-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="74610-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74610-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="74610-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74610-106">Parameters</span></span>

<span data-ttu-id="74610-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="74610-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74610-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74610-108">Return value</span></span>

<span data-ttu-id="74610-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74610-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74610-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74610-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="74610-111">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="74610-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="74610-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="74610-112">Remarks</span></span>

<span data-ttu-id="74610-113">Non è possibile usare **ID3DXSprite:: end** come sostituto di [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="74610-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74610-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74610-114">Requirements</span></span>



| <span data-ttu-id="74610-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74610-115">Requirement</span></span> | <span data-ttu-id="74610-116">Valore</span><span class="sxs-lookup"><span data-stu-id="74610-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74610-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74610-117">Header</span></span><br/>  | <dl> <span data-ttu-id="74610-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="74610-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="74610-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="74610-119">Library</span></span><br/> | <dl> <span data-ttu-id="74610-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74610-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74610-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74610-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74610-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="74610-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="74610-123">**ID3DXSprite:: Begin**</span><span class="sxs-lookup"><span data-stu-id="74610-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 




