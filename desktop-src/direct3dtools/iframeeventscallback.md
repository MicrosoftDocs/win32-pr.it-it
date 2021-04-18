---
description: Callback per restituire l'elenco di eventi in un frame.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameEventsCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304031"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="e4f31-103"><span id="vspixengine.iframeeventscallback"></span>Interfaccia IFrameEventsCallback</span><span class="sxs-lookup"><span data-stu-id="e4f31-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="e4f31-104">Callback per restituire l'elenco di eventi in un frame.</span><span class="sxs-lookup"><span data-stu-id="e4f31-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="e4f31-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e4f31-105">Members</span></span>

<span data-ttu-id="e4f31-106">L'interfaccia **IFrameEventsCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e4f31-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e4f31-107">**IFrameEventsCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4f31-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e4f31-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="e4f31-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e4f31-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="e4f31-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e4f31-110">L'interfaccia **IFrameEventsCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e4f31-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e4f31-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="e4f31-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e4f31-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f31-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e4f31-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="e4f31-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e4f31-114">Ottiene informazioni sulle colonne (tipi di dati dell'evento) supportate dall'elenco di eventi.</span><span class="sxs-lookup"><span data-stu-id="e4f31-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e4f31-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e4f31-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e4f31-116">Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e4f31-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e4f31-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4f31-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e4f31-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4f31-118">Header</span></span></p></td><td><span data-ttu-id="e4f31-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e4f31-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
