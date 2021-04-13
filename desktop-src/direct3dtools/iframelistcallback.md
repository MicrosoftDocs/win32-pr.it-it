---
description: Callback per restituire l'elenco dei frame con l'ID evento e il numero di frame.
MS-HAID: vspixengine.IFrameListCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameListCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 16318DBE-4126-4331-B726-DCF929F712DA
api_name:
- IFrameListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a4fe281584a9ca51d18eee22f7e9fd4a92e48f88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401335"
---
# <a name="span-idvspixengineiframelistcallbackspaniframelistcallback-interface"></a><span data-ttu-id="0ca55-103"><span id="vspixengine.iframelistcallback"></span>Interfaccia IFrameListCallback</span><span class="sxs-lookup"><span data-stu-id="0ca55-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback interface</span></span>

<span data-ttu-id="0ca55-104">Callback per restituire l'elenco dei frame con l'ID evento e il numero di frame.</span><span class="sxs-lookup"><span data-stu-id="0ca55-104">Callback to return the list of frames with their event id and frame number.</span></span>

## <a name="members"></a><span data-ttu-id="0ca55-105">Membri</span><span class="sxs-lookup"><span data-stu-id="0ca55-105">Members</span></span>

<span data-ttu-id="0ca55-106">L'interfaccia **IFrameListCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0ca55-106">The **IFrameListCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0ca55-107">**IFrameListCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ca55-107">**IFrameListCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0ca55-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="0ca55-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0ca55-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="0ca55-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0ca55-110">L'interfaccia **IFrameListCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0ca55-110">The **IFrameListCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0ca55-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="0ca55-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0ca55-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca55-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0ca55-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ca55-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0ca55-114">Funzione di callback utilizzata per notificare all'host i frame acquisiti.</span><span class="sxs-lookup"><span data-stu-id="0ca55-114">A callback function used to notify the host of which frames were captured.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0ca55-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ca55-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0ca55-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ca55-116">Header</span></span></p></td><td><span data-ttu-id="0ca55-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0ca55-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
