---
title: Informazioni di riferimento sull'API dell'host del dispositivo
description: Le interfacce seguenti fanno parte dell'API host del dispositivo con la tecnologia UPnP. L'host dispositivo con tecnologia UPnP supporta Microsoft Visual Basic e C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396479"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="ccdc6-104">Informazioni di riferimento sull'API dell'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ccdc6-104">Device Host API Reference</span></span>

<span data-ttu-id="ccdc6-105">Le interfacce seguenti fanno parte dell'API host del dispositivo con la tecnologia UPnP.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="ccdc6-106">L'host dispositivo con tecnologia UPnP supporta Microsoft Visual Basic e C++.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="ccdc6-107">Questa API non fornisce supporto per Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="ccdc6-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="ccdc6-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ccdc6-108">Interface</span></span>                                                  | <span data-ttu-id="ccdc6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccdc6-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccdc6-110">**IUPnPDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="ccdc6-111">Usato dall'host del dispositivo per gestire i dispositivi e i servizi correlati.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="ccdc6-112">**IUPnPDeviceProvider**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="ccdc6-113">Usato dall'host del dispositivo per avviare e arrestare i provider di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="ccdc6-114">**IUPnPEventSink**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="ccdc6-115">Usato dai dispositivi per inviare notifiche degli eventi all'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="ccdc6-116">**IUPnPEventSource**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="ccdc6-117">Usato dall'host del dispositivo per sottoscrivere o annullare la sottoscrizione agli eventi forniti dal servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="ccdc6-118">**IUPnPRegistrar**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="ccdc6-119">Usato dai dispositivi per la registrazione con l'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="ccdc6-120">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="ccdc6-121">Usato dai dispositivi per ottenere informazioni su un richiedente, ovvero un punto di controllo, e la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="ccdc6-122">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="ccdc6-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="ccdc6-123">Usato dai dispositivi per ripetere la registrazione con l'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ccdc6-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




