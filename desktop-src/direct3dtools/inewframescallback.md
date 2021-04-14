---
description: Callback dal motore che indica che è stata eseguita l'analisi di eventuali nuovi frame aggiunti al log.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401332"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="eee46-103"><span id="vspixengine.inewframescallback"></span>Interfaccia INewFramesCallback</span><span class="sxs-lookup"><span data-stu-id="eee46-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="eee46-104">Callback dal motore che indica che è stata eseguita l'analisi di eventuali nuovi frame aggiunti al log.</span><span class="sxs-lookup"><span data-stu-id="eee46-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="eee46-105">Membri</span><span class="sxs-lookup"><span data-stu-id="eee46-105">Members</span></span>

<span data-ttu-id="eee46-106">L'interfaccia **INewFramesCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eee46-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eee46-107">**INewFramesCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eee46-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="eee46-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="eee46-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="eee46-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="eee46-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="eee46-110">L'interfaccia **INewFramesCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="eee46-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="eee46-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="eee46-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="eee46-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="eee46-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="eee46-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="eee46-114">Callback che notifica all'host che tutte le richieste sono state annullate.</span><span class="sxs-lookup"><span data-stu-id="eee46-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="eee46-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="eee46-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="eee46-116">Callback che notifica all'host una richiesta annullata.</span><span class="sxs-lookup"><span data-stu-id="eee46-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="eee46-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="eee46-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="eee46-118">Callback che notifica all'host di una richiesta annullata usando un cookie che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="eee46-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="eee46-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="eee46-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="eee46-120">Callback che notifica all'host che i nuovi frame sono disponibili per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="eee46-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="eee46-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eee46-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eee46-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eee46-122">Header</span></span></p></td><td><span data-ttu-id="eee46-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eee46-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
