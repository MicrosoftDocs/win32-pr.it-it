---
description: Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'Metodo ID3DXEffect:: OnResetDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322356"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="62ee9-103">Metodo ID3DXEffect:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="62ee9-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="62ee9-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="62ee9-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ee9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62ee9-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="62ee9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62ee9-106">Parameters</span></span>

<span data-ttu-id="62ee9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="62ee9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62ee9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62ee9-108">Return value</span></span>

<span data-ttu-id="62ee9-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62ee9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62ee9-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62ee9-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="62ee9-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="62ee9-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="62ee9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="62ee9-112">Remarks</span></span>

<span data-ttu-id="62ee9-113">**ID3DXEffect:: OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima di qualsiasi altro metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="62ee9-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="62ee9-114">Si tratta di una posizione ideale per acquisire nuovamente le risorse di memoria video e i blocchi di stato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="62ee9-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ee9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62ee9-115">Requirements</span></span>



| <span data-ttu-id="62ee9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ee9-116">Requirement</span></span> | <span data-ttu-id="62ee9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="62ee9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ee9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62ee9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="62ee9-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="62ee9-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="62ee9-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="62ee9-120">Library</span></span><br/> | <dl> <span data-ttu-id="62ee9-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62ee9-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="62ee9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62ee9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ee9-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="62ee9-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
