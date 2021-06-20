---
description: Informazioni su come implementare servizi Web nei dispositivi (WSD). Comprendere lo scopo, dove è applicabile, i destinatari degli sviluppatori e i requisiti di run-time.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Servizi Web nei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405754"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="64222-104">Servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="64222-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="64222-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="64222-105">Purpose</span></span>

<span data-ttu-id="64222-106">L'API Servizi Web Microsoft nei dispositivi (WSDAPI) supporta l'implementazione di dispositivi e servizi controllati dal client e host di dispositivi conformi al profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="64222-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="64222-107">WSDAPI usa [WS-Discovery per](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) l'individuazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="64222-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="64222-108">WSDAPI può essere usato per lo sviluppo di implementazioni client e di servizio.</span><span class="sxs-lookup"><span data-stu-id="64222-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="64222-109">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="64222-109">Where applicable</span></span>

<span data-ttu-id="64222-110">Servizi Web nei dispositivi consente a un client di individuare e accedere a un dispositivo remoto e ai servizi associati in una rete.</span><span class="sxs-lookup"><span data-stu-id="64222-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="64222-111">Supporta l'individuazione, la descrizione, il controllo e l'evento dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="64222-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="64222-112">Gli sviluppatori possono creare proxy client WSDAPI e stub corrispondenti per gli host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64222-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="64222-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="64222-113">Developer audience</span></span>

<span data-ttu-id="64222-114">La documentazione relativa ai servizi Web nei dispositivi è destinata ai programmatori C/C++ e ai fornitori di dispositivi che creano prodotti conformi a DPWS.</span><span class="sxs-lookup"><span data-stu-id="64222-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="64222-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="64222-115">Run-time requirements</span></span>

<span data-ttu-id="64222-116">Le applicazioni client che usano WSDAPI sono supportate a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="64222-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64222-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="64222-117">In this section</span></span>



| <span data-ttu-id="64222-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="64222-118">Topic</span></span>                                                                                  | <span data-ttu-id="64222-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64222-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64222-120">Informazioni sui servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="64222-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="64222-121">Architettura e informazioni generali sui servizi Web nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="64222-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="64222-122">Uso di servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="64222-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="64222-123">Informazioni sulla generazione di codice, sulla configurazione delle applicazioni e sulla risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="64222-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="64222-124">Informazioni di riferimento sui servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="64222-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="64222-125">Documentazione di riferimento per l'API Servizi Web nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="64222-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="64222-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64222-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64222-127">Blog di Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="64222-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

