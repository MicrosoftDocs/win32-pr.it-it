---
description: Callback usati per la visualizzazione delle trame.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124722"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="4cd68-103"><span id="vspixengine.ipixengine5callbacks"></span>Interfaccia IPixEngine5Callbacks</span><span class="sxs-lookup"><span data-stu-id="4cd68-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="4cd68-104">Callback usati per la visualizzazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="4cd68-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="4cd68-105">Membri</span><span class="sxs-lookup"><span data-stu-id="4cd68-105">Members</span></span>

<span data-ttu-id="4cd68-106">L'interfaccia **IPixEngine5Callbacks** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4cd68-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4cd68-107">**IPixEngine5Callbacks** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4cd68-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="4cd68-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="4cd68-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4cd68-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="4cd68-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4cd68-110">L'interfaccia **IPixEngine5Callbacks** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4cd68-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4cd68-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="4cd68-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4cd68-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cd68-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4cd68-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-114">Funzione di callback utilizzata per notificare all'host quando una trama è stata liberata.</span><span class="sxs-lookup"><span data-stu-id="4cd68-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4cd68-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-116">Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di un istogramma.</span><span class="sxs-lookup"><span data-stu-id="4cd68-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4cd68-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-118">Funzione di callback utilizzata per notificare all'host quando è stato completato un caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="4cd68-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4cd68-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-120">Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di una sezione di trama.</span><span class="sxs-lookup"><span data-stu-id="4cd68-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4cd68-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-122">Funzione di callback utilizzata per notificare all'host quando un valore di Texel letto è stato completato.</span><span class="sxs-lookup"><span data-stu-id="4cd68-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4cd68-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-124">Funzione di callback utilizzata per notificare all'host quando è stato completato il rendering di una trama.</span><span class="sxs-lookup"><span data-stu-id="4cd68-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4cd68-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd68-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4cd68-126">Una funzione di callback utilizzata per notificare all'host quando il salvataggio di una trama è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4cd68-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4cd68-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cd68-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4cd68-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cd68-128">Header</span></span></p></td><td><span data-ttu-id="4cd68-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4cd68-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
