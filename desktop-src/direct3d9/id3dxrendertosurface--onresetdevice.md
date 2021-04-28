---
description: 'Metodo ID3DXRenderToSurface::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: Metodo ID3DXRenderToSurface::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17af145a236d2b3a51d271c6687d78d81a387363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107189"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a><span data-ttu-id="e60f7-103">Metodo ID3DXRenderToSurface::OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="e60f7-103">ID3DXRenderToSurface::OnResetDevice method</span></span>

<span data-ttu-id="e60f7-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="e60f7-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e60f7-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="e60f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e60f7-106">Parameters</span></span>

<span data-ttu-id="e60f7-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e60f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e60f7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e60f7-108">Return value</span></span>

<span data-ttu-id="e60f7-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e60f7-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e60f7-110">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e60f7-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e60f7-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e60f7-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e60f7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e60f7-112">Remarks</span></span>

<span data-ttu-id="e60f7-113">ID3DXRenderToSurface::OnResetDevice deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima che venga chiamato qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="e60f7-113">ID3DXRenderToSurface::OnResetDevice should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="e60f7-114">Si tratta di un buon punto per acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="e60f7-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e60f7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e60f7-115">Requirements</span></span>



| <span data-ttu-id="e60f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e60f7-116">Requirement</span></span> | <span data-ttu-id="e60f7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e60f7-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e60f7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e60f7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e60f7-119"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="e60f7-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e60f7-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e60f7-120">Library</span></span><br/> | <dl> <span data-ttu-id="e60f7-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e60f7-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e60f7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e60f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60f7-123">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="e60f7-123">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
