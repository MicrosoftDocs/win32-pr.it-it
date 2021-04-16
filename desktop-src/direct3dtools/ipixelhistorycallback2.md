---
description: Callback per restituire le intersezioni della cronologia dei pixel (livello di chiamata di richiamo) e primitive (a livello di triangolo) in due risultati diversi.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521561"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="47d7e-103"><span id="vspixengine.ipixelhistorycallback2"></span>Interfaccia IPixelHistoryCallback2</span><span class="sxs-lookup"><span data-stu-id="47d7e-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="47d7e-104">Callback per restituire le intersezioni della cronologia dei pixel (livello di chiamata di richiamo) e primitive (a livello di triangolo) in due risultati diversi.</span><span class="sxs-lookup"><span data-stu-id="47d7e-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="47d7e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="47d7e-105">Members</span></span>

<span data-ttu-id="47d7e-106">L'interfaccia **IPixelHistoryCallback2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="47d7e-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47d7e-107">**IPixelHistoryCallback2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="47d7e-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="47d7e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="47d7e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="47d7e-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="47d7e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="47d7e-110">L'interfaccia **IPixelHistoryCallback2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="47d7e-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="47d7e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="47d7e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="47d7e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47d7e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="47d7e-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="47d7e-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47d7e-114">Callback che notifica all'host le informazioni di intersezione della Cronologia pixel restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="47d7e-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="47d7e-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="47d7e-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="47d7e-116">Callback che notifica all'host le informazioni sulle operazioni primitive della Cronologia pixel restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="47d7e-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="47d7e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47d7e-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="47d7e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47d7e-118">Header</span></span></p></td><td><span data-ttu-id="47d7e-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="47d7e-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
