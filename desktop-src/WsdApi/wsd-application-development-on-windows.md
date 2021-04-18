---
description: L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al profilo dei dispositivi per i servizi Web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Sviluppo di applicazioni WSD in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312664"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="e9f34-103">Sviluppo di applicazioni WSD in Windows</span><span class="sxs-lookup"><span data-stu-id="e9f34-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="e9f34-104">L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al [profilo dei dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="e9f34-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="e9f34-105">WSDAPI può essere usato per lo sviluppo di implementazioni di client e server (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e9f34-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="e9f34-106">Abbastanza spesso, il codice WSDAPI per queste applicazioni viene generato usando [WsdCodeGen](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="e9f34-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="e9f34-107">Alcune funzioni e metodi WSDAPI sono progettati per essere chiamati solo dal codice generato.</span><span class="sxs-lookup"><span data-stu-id="e9f34-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="e9f34-108">La documentazione di riferimento dell'API indica quando una funzione o un metodo deve essere utilizzato o implementato solo dal codice generato.</span><span class="sxs-lookup"><span data-stu-id="e9f34-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="e9f34-109">Il Windows SDK include alcuni file WSDL di esempio, i file di configurazione WsdCodeGen e il codice generato.</span><span class="sxs-lookup"><span data-stu-id="e9f34-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="e9f34-110">Per ulteriori informazioni, vedere [WSDAPI Samples](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e9f34-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="e9f34-111">Se si desidera enumerare i dispositivi utilizzando il protocollo WSD ed eseguire query su metadati del dispositivo WSD, è possibile utilizzare l'API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) .</span><span class="sxs-lookup"><span data-stu-id="e9f34-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="e9f34-112">Se si desidera implementare un dispositivo WSD che non esegue Windows, vedere [WSD Device Development](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="e9f34-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
