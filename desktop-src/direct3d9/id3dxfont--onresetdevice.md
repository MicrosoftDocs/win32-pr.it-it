---
description: Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'Metodo ID3DXFont:: OnResetDevice (D3dx9core. h)'
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
ms.openlocfilehash: d6e65001f484ed7d7a984ed1f9463b996056e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401985"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="fc2e3-103">Metodo ID3DXFont:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="fc2e3-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="fc2e3-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc2e3-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="fc2e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc2e3-106">Parameters</span></span>

<span data-ttu-id="fc2e3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc2e3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc2e3-108">Return value</span></span>

<span data-ttu-id="fc2e3-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc2e3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc2e3-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fc2e3-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2e3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc2e3-112">Remarks</span></span>

<span data-ttu-id="fc2e3-113">**OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (tramite [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima di chiamare qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="fc2e3-114">Si tratta di una posizione ideale per acquisire nuovamente le risorse di memoria video e i blocchi di stato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="fc2e3-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2e3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc2e3-115">Requirements</span></span>



| <span data-ttu-id="fc2e3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc2e3-116">Requirement</span></span> | <span data-ttu-id="fc2e3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc2e3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2e3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc2e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fc2e3-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2e3-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fc2e3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc2e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="fc2e3-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc2e3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc2e3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc2e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2e3-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="fc2e3-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
