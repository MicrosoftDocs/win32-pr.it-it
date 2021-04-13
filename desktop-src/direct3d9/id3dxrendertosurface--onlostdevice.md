---
description: Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: 'Metodo ID3DXRenderToSurface:: OnLostDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18e759fb12cd13c30cf3318b7208f87f824ab9cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355829"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a><span data-ttu-id="93abb-104">Metodo ID3DXRenderToSurface:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="93abb-104">ID3DXRenderToSurface::OnLostDevice method</span></span>

<span data-ttu-id="93abb-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="93abb-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="93abb-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93abb-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="93abb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93abb-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="93abb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93abb-108">Parameters</span></span>

<span data-ttu-id="93abb-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="93abb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93abb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93abb-110">Return value</span></span>

<span data-ttu-id="93abb-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93abb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93abb-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93abb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93abb-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="93abb-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="93abb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="93abb-114">Remarks</span></span>

<span data-ttu-id="93abb-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span><span class="sxs-lookup"><span data-stu-id="93abb-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span></span> <span data-ttu-id="93abb-116">Anche se il dispositivo non è stato effettivamente perso, ID3DXRenderToSurface:: OnLostDevice è responsabile della liberazione di stateblocks e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93abb-116">Even if the device was not actually lost, ID3DXRenderToSurface::OnLostDevice is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="93abb-117">Di conseguenza, non è possibile usare nuovamente l'oggetto Font prima di chiamare **IDirect3DDevice9:: Reset** , quindi ID3DXRenderToSurface:: OnResetDevice.</span><span class="sxs-lookup"><span data-stu-id="93abb-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then ID3DXRenderToSurface::OnResetDevice.</span></span>

## <a name="requirements"></a><span data-ttu-id="93abb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93abb-118">Requirements</span></span>



| <span data-ttu-id="93abb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93abb-119">Requirement</span></span> | <span data-ttu-id="93abb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="93abb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93abb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93abb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="93abb-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="93abb-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="93abb-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="93abb-123">Library</span></span><br/> | <dl> <span data-ttu-id="93abb-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93abb-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93abb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93abb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93abb-126">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="93abb-126">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
