---
description: Valori GUID (Globally Unique Identifier) che identificano i producer dei messaggi di debug.
ms.assetid: 85946D30-5E49-4E4B-AC25-394ABFF0DB11
title: DXGI_DEBUG_ID (DXGIDebug. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc750d94fbdc51ba3399a6e3d4ff45b0adeb68b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304355"
---
# <a name="dxgi_debug_id"></a><span data-ttu-id="56236-103">\_ID debug \_ DXGI</span><span class="sxs-lookup"><span data-stu-id="56236-103">DXGI\_DEBUG\_ID</span></span>

<span data-ttu-id="56236-104">Valori GUID (Globally Unique Identifier) che identificano i producer dei messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="56236-104">Globally unique identifier (GUID) values that identify producers of debug messages.</span></span>



| <span data-ttu-id="56236-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="56236-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="56236-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56236-106">Description</span></span>                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_DEBUG_ALL"></span><span id="dxgi_debug_all"></span><dl> <span data-ttu-id="56236-107"><dt>**DXGI \_ DEBUG di \_ tutti**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xE6, 0x43, 0xE9, 0xA9, 0xcf, 0xda, 0x8</dt></span><span class="sxs-lookup"><span data-stu-id="56236-107"><dt>**DXGI\_DEBUG\_ALL**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8</dt></span></span> </dl>       | <span data-ttu-id="56236-108">Tutti gli oggetti Direct3D e DXGI e le app private.</span><span class="sxs-lookup"><span data-stu-id="56236-108">All Direct3D and DXGI objects and private apps.</span></span><br/>                                                                                     |
| <span id="DXGI_DEBUG_DX"></span><span id="dxgi_debug_dx"></span><dl> <span data-ttu-id="56236-109"><dt>**DXGI \_ DEBUG \_ DX**</dt> <dt>0x35cdd7fc, 0x13b2, 0x421d, 0xA5, 0xD7, 0x7E, 0x44, 0x51, 0x28, 0x7D, 0x64</dt></span><span class="sxs-lookup"><span data-stu-id="56236-109"><dt>**DXGI\_DEBUG\_DX**</dt> <dt>0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64</dt></span></span> </dl>         | <span data-ttu-id="56236-110">Oggetti Direct3D e DXGI.</span><span class="sxs-lookup"><span data-stu-id="56236-110">Direct3D and DXGI objects.</span></span><br/>                                                                                                          |
| <span id="DXGI_DEBUG_DXGI"></span><span id="dxgi_debug_dxgi"></span><dl> <span data-ttu-id="56236-111"><dt>**DXGI \_ DEBUG \_ DXGI**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xAC, 0x3E, 0x98, 0x87, 0x5B, 0x5a, 0x2E, 0x2A</dt></span><span class="sxs-lookup"><span data-stu-id="56236-111"><dt>**DXGI\_DEBUG\_DXGI**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a</dt></span></span> </dl>   | <span data-ttu-id="56236-112">DXGI.</span><span class="sxs-lookup"><span data-stu-id="56236-112">DXGI.</span></span><br/>                                                                                                                               |
| <span id="DXGI_DEBUG_APP"></span><span id="dxgi_debug_app"></span><dl> <span data-ttu-id="56236-113"><dt>**DXGI \_ \_App di debug**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xED, 0x23, 0x36, 0xc, 0x62</dt></span><span class="sxs-lookup"><span data-stu-id="56236-113"><dt>**DXGI\_DEBUG\_APP**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62</dt></span></span> </dl>         | <span data-ttu-id="56236-114">App private.</span><span class="sxs-lookup"><span data-stu-id="56236-114">Private apps.</span></span> <span data-ttu-id="56236-115">Tutti i messaggi aggiunti con [**IDXGIInfoQueue:: AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).</span><span class="sxs-lookup"><span data-stu-id="56236-115">Any messages that you add with [**IDXGIInfoQueue::AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).</span></span><br/> |
| <span id="DXGI_DEBUG_D3D11"></span><span id="dxgi_debug_d3d11"></span><dl> <span data-ttu-id="56236-116"><dt>**DXGI \_ DEBUG \_ d3d11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xBB, 0xb, 0xBA, messaggi 0XA0, 0x47, 0x84, 0x79, 0x8F</dt></span><span class="sxs-lookup"><span data-stu-id="56236-116"><dt>**DXGI\_DEBUG\_D3D11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f</dt></span></span> </dl> | <span data-ttu-id="56236-117">Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="56236-117">Direct3D 11.</span></span> <span data-ttu-id="56236-118">Definito in D3D11SDKLayers. h.</span><span class="sxs-lookup"><span data-stu-id="56236-118">Defined in D3D11SDKLayers.h.</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="56236-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="56236-119">Remarks</span></span>

<span data-ttu-id="56236-120">Usare questi valori con l'interfaccia [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .</span><span class="sxs-lookup"><span data-stu-id="56236-120">Use these values with the [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) interface.</span></span>

``` syntax
typedef GUID DXGI_DEBUG_ID;

DEFINE_GUID(DXGI_DEBUG_ALL, 0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8);
DEFINE_GUID(DXGI_DEBUG_DX, 0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64);
DEFINE_GUID(DXGI_DEBUG_DXGI, 0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a);
DEFINE_GUID(DXGI_DEBUG_APP, 0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62);

DEFINE_GUID(DXGI_DEBUG_D3D11, 0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f);
```

<span data-ttu-id="56236-121">Per usare uno di questi valori GUID, includere DXGIDebug. h nel codice e il collegamento a dxguid. lib.</span><span class="sxs-lookup"><span data-stu-id="56236-121">To use any of these GUID values, include DXGIDebug.h in your code and link to dxguid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="56236-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56236-122">Requirements</span></span>



| <span data-ttu-id="56236-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="56236-123">Requirement</span></span> | <span data-ttu-id="56236-124">Valore</span><span class="sxs-lookup"><span data-stu-id="56236-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56236-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56236-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56236-126">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="56236-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="56236-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56236-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56236-128">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="56236-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="56236-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56236-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="56236-130"><dt>DXGIDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="56236-130"><dt>DXGIDebug.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56236-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56236-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56236-132">Costanti DXGI</span><span class="sxs-lookup"><span data-stu-id="56236-132">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




