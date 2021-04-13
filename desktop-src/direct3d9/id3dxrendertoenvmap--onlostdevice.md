---
description: Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'Metodo ID3DXRenderToEnvMap:: OnLostDevice (D3dx9core. h)'
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
ms.openlocfilehash: b644ab595fd8bc6ebdfa544cc004598f5570d262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354524"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="0d5ad-104">Metodo ID3DXRenderToEnvMap:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="0d5ad-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="0d5ad-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="0d5ad-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5ad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d5ad-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="0d5ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d5ad-108">Parameters</span></span>

<span data-ttu-id="0d5ad-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d5ad-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d5ad-110">Return value</span></span>

<span data-ttu-id="0d5ad-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d5ad-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d5ad-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0d5ad-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5ad-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d5ad-114">Remarks</span></span>

<span data-ttu-id="0d5ad-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="0d5ad-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="0d5ad-116">Anche se il dispositivo non è stato effettivamente perso, **ID3DXRenderToEnvMap:: OnLostDevice** è responsabile della liberazione di stateblocks e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d5ad-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="0d5ad-117">Di conseguenza, non è possibile usare nuovamente l'oggetto Font prima di chiamare **IDirect3DDevice9:: Reset** , quindi [**ID3DXRenderToEnvMap:: OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d5ad-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d5ad-118">Requirements</span></span>



| <span data-ttu-id="0d5ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5ad-119">Requirement</span></span> | <span data-ttu-id="0d5ad-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0d5ad-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5ad-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d5ad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0d5ad-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5ad-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0d5ad-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d5ad-123">Library</span></span><br/> | <dl> <span data-ttu-id="0d5ad-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d5ad-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d5ad-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d5ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5ad-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="0d5ad-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




