---
description: 'Metodo ID3DXRenderToEnvMap::OnLostDevice: usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: Metodo ID3DXRenderToEnvMap::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88f27c259262eb7abb57246e547ad66866bb3dcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107199"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="9286c-104">Metodo ID3DXRenderToEnvMap::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="9286c-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="9286c-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="9286c-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="9286c-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9286c-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9286c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9286c-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="9286c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9286c-108">Parameters</span></span>

<span data-ttu-id="9286c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9286c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9286c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9286c-110">Return value</span></span>

<span data-ttu-id="9286c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9286c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9286c-112">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9286c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9286c-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9286c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9286c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9286c-114">Remarks</span></span>

<span data-ttu-id="9286c-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente [**chiami IDirect3DDevice9::Reset.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="9286c-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="9286c-116">Anche se il dispositivo non è stato effettivamente perso, **ID3DXRenderToEnvMap::OnLostDevice** è responsabile del rilascio di blocchi di stato e di altre risorse che potrebbero dover essere rilasciate prima della reimpostazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9286c-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="9286c-117">Di conseguenza, l'oggetto tipo di carattere non può essere usato di nuovo prima di chiamare **IDirect3DDevice9::Reset** e [**quindi ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9286c-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9286c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9286c-118">Requirements</span></span>



| <span data-ttu-id="9286c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9286c-119">Requirement</span></span> | <span data-ttu-id="9286c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9286c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9286c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9286c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9286c-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="9286c-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9286c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9286c-123">Library</span></span><br/> | <dl> <span data-ttu-id="9286c-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9286c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9286c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9286c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9286c-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="9286c-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




