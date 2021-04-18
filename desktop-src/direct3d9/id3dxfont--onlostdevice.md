---
description: Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'Metodo ID3DXFont:: OnLostDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322987"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="ca8f2-104">Metodo ID3DXFont:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="ca8f2-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="ca8f2-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="ca8f2-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca8f2-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="ca8f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca8f2-108">Parameters</span></span>

<span data-ttu-id="ca8f2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca8f2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca8f2-110">Return value</span></span>

<span data-ttu-id="ca8f2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca8f2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca8f2-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca8f2-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca8f2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca8f2-114">Remarks</span></span>

<span data-ttu-id="ca8f2-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ca8f2-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="ca8f2-116">Anche se il dispositivo non è stato effettivamente perso, **OnLostDevice** è responsabile di liberare stateblocks e altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca8f2-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="ca8f2-117">Di conseguenza, non è possibile usare nuovamente l'oggetto Font prima di chiamare **Reset** e quindi [**OnResetDevice**](id3dxfont--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ca8f2-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca8f2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca8f2-118">Requirements</span></span>



| <span data-ttu-id="ca8f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca8f2-119">Requirement</span></span> | <span data-ttu-id="ca8f2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ca8f2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8f2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca8f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca8f2-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca8f2-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ca8f2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca8f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca8f2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca8f2-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca8f2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca8f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8f2-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="ca8f2-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




