---
description: Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.
ms.assetid: 74f8616e-c3ed-4231-b701-009213ea48c0
title: 'Metodo ID3DXSprite:: OnResetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09e08a32aca8df0577a5fb73ef09ec69742556b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322970"
---
# <a name="id3dxspriteonresetdevice-method"></a><span data-ttu-id="12974-103">Metodo ID3DXSprite:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="12974-103">ID3DXSprite::OnResetDevice method</span></span>

<span data-ttu-id="12974-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="12974-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="12974-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12974-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="12974-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12974-106">Parameters</span></span>

<span data-ttu-id="12974-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="12974-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12974-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12974-108">Return value</span></span>

<span data-ttu-id="12974-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12974-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12974-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12974-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12974-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="12974-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="12974-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="12974-112">Remarks</span></span>

<span data-ttu-id="12974-113">**ID3DXSprite:: OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima di qualsiasi altro metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="12974-113">**ID3DXSprite::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="12974-114">Si tratta di una posizione ideale per acquisire nuovamente le risorse di memoria video e i blocchi di stato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="12974-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="12974-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12974-115">Requirements</span></span>



| <span data-ttu-id="12974-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="12974-116">Requirement</span></span> | <span data-ttu-id="12974-117">Valore</span><span class="sxs-lookup"><span data-stu-id="12974-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12974-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12974-118">Header</span></span><br/>  | <dl> <span data-ttu-id="12974-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="12974-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="12974-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="12974-120">Library</span></span><br/> | <dl> <span data-ttu-id="12974-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12974-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12974-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12974-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12974-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="12974-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
