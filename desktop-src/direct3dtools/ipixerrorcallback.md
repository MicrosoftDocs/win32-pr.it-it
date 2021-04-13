---
description: Callback dal motore per gestire gli errori.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixErrorCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401134"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="5afa5-103"><span id="vspixengine.ipixerrorcallback"></span>Interfaccia IPixErrorCallback</span><span class="sxs-lookup"><span data-stu-id="5afa5-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="5afa5-104">Callback dal motore per gestire gli errori.</span><span class="sxs-lookup"><span data-stu-id="5afa5-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="5afa5-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5afa5-105">Members</span></span>

<span data-ttu-id="5afa5-106">L'interfaccia **IPixErrorCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5afa5-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5afa5-107">**IPixErrorCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5afa5-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="5afa5-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5afa5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="5afa5-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="5afa5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="5afa5-110">L'interfaccia **IPixErrorCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5afa5-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="5afa5-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5afa5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="5afa5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5afa5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5afa5-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="5afa5-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5afa5-114">Callback che notifica all'host gli errori restituiti dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="5afa5-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="5afa5-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="5afa5-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5afa5-116">Callback che invia una notifica all'host dei messaggi restituiti dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="5afa5-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5afa5-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="5afa5-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5afa5-118">Callback che notifica all'host gli avvisi restituiti dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="5afa5-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="5afa5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5afa5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5afa5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5afa5-120">Header</span></span></p></td><td><span data-ttu-id="5afa5-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5afa5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
