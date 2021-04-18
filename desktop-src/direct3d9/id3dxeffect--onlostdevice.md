---
description: Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'Metodo ID3DXEffect:: OnLostDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af2d17c99f0b694a8b27924c34faa2a1f633fafb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322357"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="5de2b-104">Metodo ID3DXEffect:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="5de2b-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="5de2b-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="5de2b-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="5de2b-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5de2b-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de2b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5de2b-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="5de2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5de2b-108">Parameters</span></span>

<span data-ttu-id="5de2b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5de2b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5de2b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5de2b-110">Return value</span></span>

<span data-ttu-id="5de2b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5de2b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5de2b-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5de2b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5de2b-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5de2b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de2b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5de2b-114">Remarks</span></span>

<span data-ttu-id="5de2b-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="5de2b-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="5de2b-116">Anche se il dispositivo non è stato effettivamente perso, **ID3DXEffect:: OnLostDevice** è responsabile della liberazione di stateblocks e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5de2b-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="5de2b-117">Di conseguenza, non è possibile usare nuovamente l'oggetto Font prima di chiamare **IDirect3DDevice9:: Reset** , quindi [**ID3DXEffect:: OnResetDevice**](id3dxeffect--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="5de2b-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5de2b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5de2b-118">Requirements</span></span>



| <span data-ttu-id="5de2b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de2b-119">Requirement</span></span> | <span data-ttu-id="5de2b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5de2b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de2b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5de2b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5de2b-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de2b-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5de2b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5de2b-123">Library</span></span><br/> | <dl> <span data-ttu-id="5de2b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de2b-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5de2b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5de2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de2b-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="5de2b-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




