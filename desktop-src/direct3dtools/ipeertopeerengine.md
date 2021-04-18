---
description: Interfaccia per la comunicazione remota dei dati su un vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304056"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="4c662-103"><span id="vspixengine.ipeertopeerengine"></span>Interfaccia IPeerToPeerEngine</span><span class="sxs-lookup"><span data-stu-id="4c662-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="4c662-104">Interfaccia per la comunicazione remota dei dati su un vsglog.</span><span class="sxs-lookup"><span data-stu-id="4c662-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="4c662-105">Membri</span><span class="sxs-lookup"><span data-stu-id="4c662-105">Members</span></span>

<span data-ttu-id="4c662-106">L'interfaccia **IPeerToPeerEngine** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4c662-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4c662-107">**IPeerToPeerEngine** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4c662-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="4c662-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="4c662-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4c662-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="4c662-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4c662-110">L'interfaccia **IPeerToPeerEngine** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4c662-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4c662-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="4c662-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4c662-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c662-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4c662-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c662-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4c662-114">Annulla una richiesta precedente per impostare una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="4c662-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4c662-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c662-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4c662-116">Ottiene l'indirizzo dell'endpoint di un motore remoto.</span><span class="sxs-lookup"><span data-stu-id="4c662-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4c662-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c662-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4c662-118">Imposta l'indirizzo dell'endpoint utilizzato per la connessione a un motore remoto.</span><span class="sxs-lookup"><span data-stu-id="4c662-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4c662-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c662-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4c662-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c662-120">Header</span></span></p></td><td><span data-ttu-id="4c662-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4c662-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
