---
description: '<span id="vspixengine.ipipelinestagesrequest2"></span>Interfaccia IPipeLineStagesRequest2: non usata. In precedenza una richiesta per i dati delle fasi della pipeline.'
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPipeLineStagesRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107069"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="a19e5-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Interfaccia IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="a19e5-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="a19e5-105">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a19e5-105">Not used.</span></span> <span data-ttu-id="a19e5-106">In precedenza una richiesta per i dati delle fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a19e5-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="a19e5-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a19e5-107">Members</span></span>

<span data-ttu-id="a19e5-108">**L'interfaccia IPipeLineStagesRequest2** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="a19e5-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a19e5-109">**IPipeLineStagesRequest2** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a19e5-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="a19e5-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a19e5-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a19e5-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="a19e5-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a19e5-112">**L'interfaccia IPipeLineStagesRequest2** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a19e5-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a19e5-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a19e5-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a19e5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a19e5-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a19e5-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="a19e5-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a19e5-116">Richiesta asincrona per ottenere i dati dello shader di calcolo per l'invio specificato.</span><span class="sxs-lookup"><span data-stu-id="a19e5-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a19e5-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="a19e5-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a19e5-118">Richiesta asincrona per ottenere se la fase dello shader di calcolo è stata usata per il frame e l'evento specificati.</span><span class="sxs-lookup"><span data-stu-id="a19e5-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a19e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a19e5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a19e5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a19e5-120">Header</span></span></p></td><td><span data-ttu-id="a19e5-121">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="a19e5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
