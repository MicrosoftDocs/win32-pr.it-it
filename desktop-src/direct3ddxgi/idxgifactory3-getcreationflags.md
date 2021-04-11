---
description: Ottiene i flag utilizzati durante la creazione di un oggetto Microsoft DirectX Graphics Infrastructure (DXGI).
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'Metodo IDXGIFactory3:: GetCreationFlags'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123324"
---
# <a name="idxgifactory3getcreationflags-method"></a><span data-ttu-id="14073-103">Metodo IDXGIFactory3:: GetCreationFlags</span><span class="sxs-lookup"><span data-stu-id="14073-103">IDXGIFactory3::GetCreationFlags method</span></span>

<span data-ttu-id="14073-104">Ottiene i flag utilizzati durante la creazione di un oggetto Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="14073-104">Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.</span></span>

## <a name="syntax"></a><span data-ttu-id="14073-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14073-105">Syntax</span></span>


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a><span data-ttu-id="14073-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14073-106">Parameters</span></span>

<span data-ttu-id="14073-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="14073-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14073-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14073-108">Return value</span></span>

<span data-ttu-id="14073-109">Flag di creazione.</span><span class="sxs-lookup"><span data-stu-id="14073-109">The creation flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="14073-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="14073-110">Remarks</span></span>

<span data-ttu-id="14073-111">Il metodo **GetCreationFlags** restituisce i flag passati alla funzione [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) o sono stati costruiti in modo implicito da [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="14073-111">The **GetCreationFlags** method returns flags that were passed to the [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) function, or were implicitly constructed by [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice), or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="see-also"></a><span data-ttu-id="14073-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14073-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14073-113">**IDXGIFactory3**</span><span class="sxs-lookup"><span data-stu-id="14073-113">**IDXGIFactory3**</span></span>](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
