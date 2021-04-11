---
description: Richiesta di intersezione e primitive della Cronologia pixel separatamente.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixelHistoryRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789829d85f4cb986de694470a8cebddf3f26675
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342106"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span data-ttu-id="1aa03-103"><span id="vspixengine.ipixelhistoryrequest2"></span>Interfaccia IPixelHistoryRequest2</span><span class="sxs-lookup"><span data-stu-id="1aa03-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2 interface</span></span>

<span data-ttu-id="1aa03-104">Richiesta di intersezione e primitive della Cronologia pixel separatamente.</span><span class="sxs-lookup"><span data-stu-id="1aa03-104">Request for pixel history intersections and primitives separately.</span></span>

## <a name="members"></a><span data-ttu-id="1aa03-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1aa03-105">Members</span></span>

<span data-ttu-id="1aa03-106">L'interfaccia **IPixelHistoryRequest2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1aa03-106">The **IPixelHistoryRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1aa03-107">**IPixelHistoryRequest2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1aa03-107">**IPixelHistoryRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="1aa03-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1aa03-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1aa03-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="1aa03-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1aa03-110">L'interfaccia **IPixelHistoryRequest2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1aa03-110">The **IPixelHistoryRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1aa03-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1aa03-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1aa03-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1aa03-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1aa03-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span><span class="sxs-lookup"><span data-stu-id="1aa03-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1aa03-114">Richiede un elenco di eventi che generano una modifica nel pixel, nella destinazione di rendering/UAV e nel frame specificati.</span><span class="sxs-lookup"><span data-stu-id="1aa03-114">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="1aa03-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span><span class="sxs-lookup"><span data-stu-id="1aa03-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1aa03-116">Richiede un elenco di primitive da una particolare intersezione.</span><span class="sxs-lookup"><span data-stu-id="1aa03-116">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="1aa03-117">Per ulteriori informazioni, vedere la funzione membro RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="1aa03-117">For more information, see the RequestIntersections member function.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1aa03-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1aa03-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1aa03-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1aa03-119">Header</span></span></p></td><td><span data-ttu-id="1aa03-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1aa03-120">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
