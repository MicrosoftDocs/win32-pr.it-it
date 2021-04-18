---
description: L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al profilo dei dispositivi per i servizi Web (DPWS).
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Servizi Web nei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309742"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="eda85-103">Servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="eda85-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="eda85-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="eda85-104">Purpose</span></span>

<span data-ttu-id="eda85-105">L'API Microsoft Web Services on Devices (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e degli host di dispositivi conformi al [profilo dei dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="eda85-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="eda85-106">WSDAPI USA [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) per l'individuazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eda85-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="eda85-107">WSDAPI può essere usato per lo sviluppo di implementazioni di client e servizi.</span><span class="sxs-lookup"><span data-stu-id="eda85-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="eda85-108">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="eda85-108">Where applicable</span></span>

<span data-ttu-id="eda85-109">I servizi Web nei dispositivi consentono a un client di individuare e accedere a un dispositivo remoto e ai relativi servizi associati in una rete.</span><span class="sxs-lookup"><span data-stu-id="eda85-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="eda85-110">Supporta l'individuazione, la descrizione, il controllo e gli eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eda85-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="eda85-111">Gli sviluppatori possono creare proxy client WSDAPI e Stub corrispondenti per gli host di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eda85-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="eda85-112">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="eda85-112">Developer audience</span></span>

<span data-ttu-id="eda85-113">La documentazione relativa ai servizi Web nei dispositivi è destinata ai programmatori C/C++ e ai fornitori di dispositivi che creano prodotti conformi a DPWS.</span><span class="sxs-lookup"><span data-stu-id="eda85-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="eda85-114">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="eda85-114">Run-time requirements</span></span>

<span data-ttu-id="eda85-115">Le applicazioni client che utilizzano WSDAPI sono supportate a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="eda85-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eda85-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="eda85-116">In this section</span></span>



| <span data-ttu-id="eda85-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="eda85-117">Topic</span></span>                                                                                  | <span data-ttu-id="eda85-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eda85-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eda85-119">Informazioni sui servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="eda85-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="eda85-120">Informazioni generali e sull'architettura dei servizi Web nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eda85-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="eda85-121">Uso dei servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="eda85-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="eda85-122">Informazioni sulla generazione di codice, sulla configurazione delle applicazioni e sulla risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="eda85-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="eda85-123">Guida di riferimento ai servizi Web sui dispositivi</span><span class="sxs-lookup"><span data-stu-id="eda85-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="eda85-124">Documentazione di riferimento per l'API dei servizi Web nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eda85-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="eda85-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eda85-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda85-126">Blog di Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="eda85-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

