---
description: 'Metodo ID3DXLine::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: Metodo ID3DXLine::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7e1275e7a7ec894601dc67503e25e1fa82545f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093659"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="7c15f-103">Metodo ID3DXLine::OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="7c15f-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="7c15f-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="7c15f-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c15f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c15f-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="7c15f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c15f-106">Parameters</span></span>

<span data-ttu-id="7c15f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7c15f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c15f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c15f-108">Return value</span></span>

<span data-ttu-id="7c15f-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c15f-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c15f-110">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c15f-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7c15f-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7c15f-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c15f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c15f-112">Remarks</span></span>

<span data-ttu-id="7c15f-113">**ID3DXLine::OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9::Reset)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima di chiamare qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="7c15f-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="7c15f-114">Si tratta di un buon punto in cui è possibile acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="7c15f-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c15f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c15f-115">Requirements</span></span>



| <span data-ttu-id="7c15f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c15f-116">Requirement</span></span> | <span data-ttu-id="7c15f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7c15f-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c15f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c15f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7c15f-119"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="7c15f-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7c15f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c15f-120">Library</span></span><br/> | <dl> <span data-ttu-id="7c15f-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c15f-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c15f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c15f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c15f-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="7c15f-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
