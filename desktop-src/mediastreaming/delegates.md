---
title: Delegati
description: L'API di streaming multimediale fornisce le funzioni del gestore eventi seguenti.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516743"
---
# <a name="delegates"></a><span data-ttu-id="88d3e-103">Delegati</span><span class="sxs-lookup"><span data-stu-id="88d3e-103">Delegates</span></span>

<span data-ttu-id="88d3e-104">L' [API di streaming multimediale](media-streaming-api-portal.md) fornisce le funzioni del gestore eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="88d3e-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="88d3e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="88d3e-105">In this section</span></span>



| <span data-ttu-id="88d3e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="88d3e-106">Topic</span></span>                                                                                   | <span data-ttu-id="88d3e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88d3e-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d3e-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88d3e-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="88d3e-109">Rappresenta la funzione che gestirà l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) che notifica al client le modifiche apportate allo stato della connessione di rete del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88d3e-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="88d3e-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88d3e-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="88d3e-111">Rappresenta la funzione che gestirà gli eventi [**DeviceArrival**](devicearrival.md) e [**DeviceDeparture**](devicedeparture.md) che notificano al client le modifiche nell'elenco dei dispositivi memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="88d3e-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="88d3e-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88d3e-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="88d3e-113">Rappresenta la funzione che gestirà l'evento [**RenderingParametersUpdate**](renderingparametersupdate.md) che invia una notifica al client di un aggiornamento a uno dei parametri del controllo di rendering di ricevitore.</span><span class="sxs-lookup"><span data-stu-id="88d3e-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="88d3e-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88d3e-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="88d3e-115">Rappresenta la funzione che gestirà l'evento [**TransportParametersUpdate**](transportparametersupdate.md) che invia una notifica al client di un aggiornamento a uno dei parametri di trasporto di ricevitore s.</span><span class="sxs-lookup"><span data-stu-id="88d3e-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

