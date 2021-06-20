---
description: Informazioni su come usare l'API WSD (Microsoft Web Services on Devices) per implementare dispositivi e servizi controllati dal client e host dei dispositivi conformi a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Sviluppo di applicazioni WSD in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405784"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="4cc78-103">Sviluppo di applicazioni WSD in Windows</span><span class="sxs-lookup"><span data-stu-id="4cc78-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="4cc78-104">L'API Servizi Web Microsoft nei dispositivi (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e di host di dispositivi conformi al profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="4cc78-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="4cc78-105">WSDAPI può essere usato per lo sviluppo di implementazioni client e server (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="4cc78-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="4cc78-106">Molto spesso il codice WSDAPI per queste applicazioni viene generato [usando WsdCodeGen.](web-services-for-devices-code-generator.md)</span><span class="sxs-lookup"><span data-stu-id="4cc78-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="4cc78-107">Alcune funzioni e metodi WSDAPI devono essere chiamati solo dal codice generato.</span><span class="sxs-lookup"><span data-stu-id="4cc78-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="4cc78-108">La documentazione di riferimento dell'API indica quando una funzione o un metodo deve essere usato o implementato solo dal codice generato.</span><span class="sxs-lookup"><span data-stu-id="4cc78-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="4cc78-109">Il Windows SDK include alcuni file WSDL di esempio, file di configurazione WsdCodeGen e codice generato.</span><span class="sxs-lookup"><span data-stu-id="4cc78-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="4cc78-110">Per altre informazioni, vedere [Esempi di WSDAPI.](wsdapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="4cc78-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="4cc78-111">Se si desidera enumerare i dispositivi usando il protocollo WSD ed eseguire query sui metadati dei dispositivi WSD, è possibile usare l'API [di individuazione delle](/previous-versions/windows/desktop/fundisc/fd-portal) funzioni.</span><span class="sxs-lookup"><span data-stu-id="4cc78-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="4cc78-112">Se si vuole implementare un dispositivo WSD che non esegue Windows, vedere [Sviluppo di dispositivi WSD.](wsd-device-development.md)</span><span class="sxs-lookup"><span data-stu-id="4cc78-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
