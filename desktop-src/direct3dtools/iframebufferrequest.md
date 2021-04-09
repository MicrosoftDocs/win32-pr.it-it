---
description: Callback per richiedere una destinazione di rendering.
MS-HAID: vspixengine.IFrameBufferRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameBufferRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 74497395-9956-430A-AB75-F1FD2FC4E66E
api_name:
- IFrameBufferRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 443f81cb227d76329814131acee163e1a947de8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876621"
---
# <a name="span-idvspixengineiframebufferrequestspaniframebufferrequest-interface"></a><span data-ttu-id="98256-103"><span id="vspixengine.iframebufferrequest"></span>Interfaccia IFrameBufferRequest</span><span class="sxs-lookup"><span data-stu-id="98256-103"><span id="vspixengine.iframebufferrequest"></span>IFrameBufferRequest interface</span></span>

<span data-ttu-id="98256-104">Callback per richiedere una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="98256-104">Callback to request a render target.</span></span>

## <a name="members"></a><span data-ttu-id="98256-105">Membri</span><span class="sxs-lookup"><span data-stu-id="98256-105">Members</span></span>

<span data-ttu-id="98256-106">L'interfaccia **IFrameBufferRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="98256-106">The **IFrameBufferRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="98256-107">**IFrameBufferRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="98256-107">**IFrameBufferRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="98256-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="98256-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="98256-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="98256-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="98256-110">L'interfaccia **IFrameBufferRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="98256-110">The **IFrameBufferRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="98256-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="98256-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="98256-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98256-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="98256-113"><a href="/windows/desktop/direct3dtools/iframebufferrequest-requestasync-dword-eventid-dword-iframebuffercallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="98256-113"><a href="/windows/desktop/direct3dtools/iframebufferrequest-requestasync-dword-eventid-dword-iframebuffercallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="98256-114">Richiede l'output del framebuffer della destinazione di rendering, dell'evento e del frame specificati.</span><span class="sxs-lookup"><span data-stu-id="98256-114">Requests framebuffer output of the specified render target, event, and frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="98256-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98256-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="98256-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98256-116">Header</span></span></p></td><td><span data-ttu-id="98256-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="98256-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
