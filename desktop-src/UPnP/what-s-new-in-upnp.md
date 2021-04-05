---
title: Novità delle API UPnP
description: Per le API™ UPnP sono disponibili nuove funzionalità e una documentazione aggiornata per Windows XP SP2. La tabella seguente identifica la nuova documentazione.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714350"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="3e23f-104">Novità delle API UPnP</span><span class="sxs-lookup"><span data-stu-id="3e23f-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="3e23f-105">Per le API™ UPnP sono disponibili nuove funzionalità e una documentazione aggiornata per Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="3e23f-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="3e23f-106">La tabella seguente identifica la nuova documentazione.</span><span class="sxs-lookup"><span data-stu-id="3e23f-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="3e23f-107">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="3e23f-107">Feature</span></span>                                                          | <span data-ttu-id="3e23f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e23f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e23f-109">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="3e23f-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="3e23f-110">Questa nuova interfaccia consente a un dispositivo ospitato di ottenere informazioni su un richiedente, ovvero un punto di controllo, e la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3e23f-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="3e23f-111">Sono inclusi tre metodi, ognuno dei quali fornisce un tipo diverso di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3e23f-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="3e23f-112">Implementazione del comportamento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e23f-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="3e23f-113">In questo argomento è inclusa una nuova sezione in cui viene illustrato come ottenere informazioni sugli endpoint tramite la nuova interfaccia [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="3e23f-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="3e23f-114">Impostazioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="3e23f-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="3e23f-115">Questo nuovo argomento fornisce informazioni sulle impostazioni del registro di sistema che influiscono sul comportamento delle API UPnP.</span><span class="sxs-lookup"><span data-stu-id="3e23f-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="3e23f-116">Codici di errore del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e23f-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="3e23f-117">Questo nuovo argomento illustra come un codice di errore di un dispositivo viene convertito in un valore HRESULT e viceversa.</span><span class="sxs-lookup"><span data-stu-id="3e23f-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="3e23f-118">È necessario comprendere questo processo per valutare un valore HRESULT restituito dai metodi [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) .</span><span class="sxs-lookup"><span data-stu-id="3e23f-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




