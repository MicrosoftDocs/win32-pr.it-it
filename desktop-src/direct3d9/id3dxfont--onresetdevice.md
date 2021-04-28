---
description: 'Metodo ID3DXFont::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: Metodo ID3DXFont::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d976c29d370887362e46899c7fb2a654d6e2cc7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093739"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="810cd-103">Metodo ID3DXFont::OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="810cd-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="810cd-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="810cd-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="810cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="810cd-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="810cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="810cd-106">Parameters</span></span>

<span data-ttu-id="810cd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="810cd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="810cd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="810cd-108">Return value</span></span>

<span data-ttu-id="810cd-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="810cd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="810cd-110">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="810cd-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="810cd-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="810cd-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="810cd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="810cd-112">Remarks</span></span>

<span data-ttu-id="810cd-113">**OnResetDevice deve** essere chiamato ogni volta che il dispositivo viene reimpostato (tramite [**Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima di chiamare qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="810cd-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="810cd-114">Si tratta di un buon punto in cui è possibile acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="810cd-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="810cd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="810cd-115">Requirements</span></span>



| <span data-ttu-id="810cd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="810cd-116">Requirement</span></span> | <span data-ttu-id="810cd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="810cd-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="810cd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="810cd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="810cd-119"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="810cd-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="810cd-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="810cd-120">Library</span></span><br/> | <dl> <span data-ttu-id="810cd-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="810cd-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="810cd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="810cd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810cd-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="810cd-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
