---
description: 'Metodo ID3DXSprite::OnLostDevice: usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.'
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: Metodo ID3DXSprite::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5515945ec8575937a90eb719eca4efd681be5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117779"
---
# <a name="id3dxspriteonlostdevice-method"></a><span data-ttu-id="8a08b-104">Metodo ID3DXSprite::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="8a08b-104">ID3DXSprite::OnLostDevice method</span></span>

<span data-ttu-id="8a08b-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="8a08b-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="8a08b-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a08b-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a08b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a08b-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="8a08b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a08b-108">Parameters</span></span>

<span data-ttu-id="8a08b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8a08b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a08b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a08b-110">Return value</span></span>

<span data-ttu-id="8a08b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a08b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a08b-112">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a08b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8a08b-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8a08b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a08b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a08b-114">Remarks</span></span>

<span data-ttu-id="8a08b-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente [**chiami IDirect3DDevice9::Reset.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="8a08b-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="8a08b-116">Anche se il dispositivo non è stato effettivamente perso, **ID3DXSprite::OnLostDevice** è responsabile dello sblocco degli blocchi di stato e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a08b-116">Even if the device was not actually lost, **ID3DXSprite::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="8a08b-117">Di conseguenza, l'oggetto tipo di carattere non può essere usato di nuovo prima di chiamare **IDirect3DDevice9::Reset** e [**quindi ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8a08b-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a08b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a08b-118">Requirements</span></span>



| <span data-ttu-id="8a08b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a08b-119">Requirement</span></span> | <span data-ttu-id="8a08b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8a08b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a08b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a08b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a08b-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="8a08b-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8a08b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a08b-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a08b-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a08b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a08b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a08b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a08b-126">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="8a08b-126">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




