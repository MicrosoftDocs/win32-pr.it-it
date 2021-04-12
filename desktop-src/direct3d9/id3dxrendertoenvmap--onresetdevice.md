---
description: Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: 'Metodo ID3DXRenderToEnvMap:: OnResetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d429c08d8bad23652a080998b6a4735132522ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354519"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a><span data-ttu-id="a56f3-103">Metodo ID3DXRenderToEnvMap:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="a56f3-103">ID3DXRenderToEnvMap::OnResetDevice method</span></span>

<span data-ttu-id="a56f3-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="a56f3-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a56f3-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="a56f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a56f3-106">Parameters</span></span>

<span data-ttu-id="a56f3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a56f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a56f3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a56f3-108">Return value</span></span>

<span data-ttu-id="a56f3-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a56f3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a56f3-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a56f3-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a56f3-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a56f3-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56f3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a56f3-112">Remarks</span></span>

<span data-ttu-id="a56f3-113">**ID3DXRenderToEnvMap:: OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima di qualsiasi altro metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="a56f3-113">**ID3DXRenderToEnvMap::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="a56f3-114">Si tratta di una posizione ideale per acquisire nuovamente le risorse di memoria video e i blocchi di stato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a56f3-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56f3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a56f3-115">Requirements</span></span>



| <span data-ttu-id="a56f3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56f3-116">Requirement</span></span> | <span data-ttu-id="a56f3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a56f3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a56f3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a56f3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a56f3-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a56f3-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a56f3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="a56f3-120">Library</span></span><br/> | <dl> <span data-ttu-id="a56f3-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a56f3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a56f3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a56f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56f3-123">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a56f3-123">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
