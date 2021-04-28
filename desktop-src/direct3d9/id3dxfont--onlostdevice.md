---
description: 'Metodo ID3DXFont::OnLostDevice: usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.'
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: Metodo ID3DXFont::OnLostDevice (D3dx9core.h)
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
ms.openlocfilehash: 9c484d7867745805e29bda88e2f8d49ca8bc21be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090369"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="f8631-104">Metodo ID3DXFont::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="f8631-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="f8631-105">Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="f8631-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="f8631-106">Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8631-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8631-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8631-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="f8631-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8631-108">Parameters</span></span>

<span data-ttu-id="f8631-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f8631-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8631-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8631-110">Return value</span></span>

<span data-ttu-id="f8631-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8631-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8631-112">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8631-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f8631-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8631-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8631-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8631-114">Remarks</span></span>

<span data-ttu-id="f8631-115">Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**Reset.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="f8631-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="f8631-116">Anche se il dispositivo non è stato effettivamente perso, **OnLostDevice** è responsabile del rilascio di blocchi di stato e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8631-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="f8631-117">Di conseguenza, l'oggetto tipo di carattere non può essere usato di nuovo prima **di chiamare Reset** e quindi [**OnResetDevice.**](id3dxfont--onresetdevice.md)</span><span class="sxs-lookup"><span data-stu-id="f8631-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8631-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8631-118">Requirements</span></span>



| <span data-ttu-id="f8631-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8631-119">Requirement</span></span> | <span data-ttu-id="f8631-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8631-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8631-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8631-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f8631-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8631-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f8631-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8631-123">Library</span></span><br/> | <dl> <span data-ttu-id="f8631-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8631-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8631-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8631-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8631-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="f8631-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




