---
description: Non usato. In precedenza una richiesta per i dati delle fasi della pipeline.
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPipeLineStagesRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4dfa67e0770b1c709ee80bffd01831859ad4c45a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304189"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="41666-104"><span id="vspixengine.ipipelinestagesrequest"></span>Interfaccia IPipeLineStagesRequest</span><span class="sxs-lookup"><span data-stu-id="41666-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="41666-105">Non usato.</span><span class="sxs-lookup"><span data-stu-id="41666-105">Not used.</span></span> <span data-ttu-id="41666-106">In precedenza una richiesta per i dati delle fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="41666-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="41666-107">Membri</span><span class="sxs-lookup"><span data-stu-id="41666-107">Members</span></span>

<span data-ttu-id="41666-108">L'interfaccia **IPipeLineStagesRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="41666-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="41666-109">**IPipeLineStagesRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="41666-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="41666-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="41666-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="41666-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="41666-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="41666-112">L'interfaccia **IPipeLineStagesRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="41666-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="41666-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="41666-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="41666-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41666-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="41666-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="41666-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="41666-116">Richiesta asincrona di ottenere immagini di anteprima per la finestra Fasi pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="41666-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="41666-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="41666-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="41666-118">Richiesta asincrona per ottenere un elenco di fasi usate per il frame e l'evento specificati.</span><span class="sxs-lookup"><span data-stu-id="41666-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="41666-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41666-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="41666-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41666-120">Header</span></span></p></td><td><span data-ttu-id="41666-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="41666-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
