---
description: Callback per restituire una destinazione di rendering. Il formato della destinazione di rendering restituita è R8G8B8A8 \_ UNORM indipendentemente dal formato del renderTarget nel motore.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401231"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="b5bdd-104"><span id="vspixengine.iframebuffercallback"></span>Interfaccia IFrameBufferCallback</span><span class="sxs-lookup"><span data-stu-id="b5bdd-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="b5bdd-105">Callback per restituire una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b5bdd-105">Callback to return a render target.</span></span> <span data-ttu-id="b5bdd-106">Il formato della destinazione di rendering restituita è R8G8B8A8 \_ UNORM indipendentemente dal formato del renderTarget nel motore.</span><span class="sxs-lookup"><span data-stu-id="b5bdd-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="b5bdd-107">Membri</span><span class="sxs-lookup"><span data-stu-id="b5bdd-107">Members</span></span>

<span data-ttu-id="b5bdd-108">L'interfaccia **IFrameBufferCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b5bdd-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b5bdd-109">**IFrameBufferCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b5bdd-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="b5bdd-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b5bdd-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="b5bdd-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="b5bdd-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="b5bdd-112">L'interfaccia **IFrameBufferCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b5bdd-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="b5bdd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="b5bdd-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="b5bdd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5bdd-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b5bdd-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="b5bdd-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b5bdd-116">Callback che notifica all'host le informazioni sul framebuffer restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="b5bdd-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="b5bdd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5bdd-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b5bdd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5bdd-118">Header</span></span></p></td><td><span data-ttu-id="b5bdd-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b5bdd-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
