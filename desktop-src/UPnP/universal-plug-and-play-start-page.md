---
title: API per dispositivi UPnP
description: Il Framework UPnP consente la rete dinamica di Appliance intelligenti, dispositivi wireless e PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118614"
---
# <a name="upnp-apis"></a><span data-ttu-id="78b0b-104">API per dispositivi UPnP</span><span class="sxs-lookup"><span data-stu-id="78b0b-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="78b0b-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="78b0b-105">Purpose</span></span>

<span data-ttu-id="78b0b-106">Il Framework UPnP consente la rete dinamica di Appliance intelligenti, dispositivi wireless e PC.</span><span class="sxs-lookup"><span data-stu-id="78b0b-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="78b0b-107">Sono disponibili due API per l'uso di dispositivi certificati da UPnP:</span><span class="sxs-lookup"><span data-stu-id="78b0b-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="78b0b-108">API del punto di controllo, che è costituita da un set di interfacce COM usate per trovare e controllare i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="78b0b-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="78b0b-109">L'API host del dispositivo, che è costituita da un set di interfacce COM usate per implementare i dispositivi ospitati da un computer.</span><span class="sxs-lookup"><span data-stu-id="78b0b-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="78b0b-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="78b0b-110">Where applicable</span></span>

<span data-ttu-id="78b0b-111">L'API del punto di controllo consente agli sviluppatori di scrivere applicazioni per la ricerca e il controllo dei dispositivi certificati UPnP.</span><span class="sxs-lookup"><span data-stu-id="78b0b-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="78b0b-112">L'API host del dispositivo consente agli sviluppatori di implementare la funzionalità di dispositivi certificati da UPnP e di usare l'host del dispositivo per gestire le funzioni di individuazione, descrizione, controllo, presentazione e evento di un dispositivo certificato UPnP.</span><span class="sxs-lookup"><span data-stu-id="78b0b-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="78b0b-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="78b0b-113">Developer audience</span></span>

<span data-ttu-id="78b0b-114">Gli sviluppatori che usano le API del punto di controllo e le API host del dispositivo devono avere familiarità con l'architettura del dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="78b0b-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="78b0b-115">Per ulteriori informazioni, vedere la [documentazione sull'implementazione di UPnP](https://openconnectivity.org/resources/upnpresources.zip) e il [Forum di UPnP](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="78b0b-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="78b0b-116">Gli sviluppatori che usano le API host del dispositivo devono avere familiarità con le interfacce Active Template Library (ATL) e COM.</span><span class="sxs-lookup"><span data-stu-id="78b0b-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="78b0b-117">Le API del punto di controllo e le API dell'host del dispositivo sono utilizzate da un'ampia gamma di applicazioni, dagli script incorporati nelle pagine HTML ai programmi completi C++ e Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="78b0b-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="78b0b-118">Solo l'API del punto di controllo supporta Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="78b0b-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="78b0b-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="78b0b-119">Run-time requirements</span></span>

<span data-ttu-id="78b0b-120">L'API del punto di controllo viene utilizzata in computer che eseguono Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional e Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="78b0b-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="78b0b-121">L'API host del dispositivo viene utilizzata in computer che eseguono Windows XP, Windows XP Professional e Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="78b0b-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="78b0b-122">Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere la sezione relativa ai requisiti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="78b0b-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78b0b-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="78b0b-123">In this section</span></span>



| <span data-ttu-id="78b0b-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="78b0b-124">Topic</span></span>                                                                                          | <span data-ttu-id="78b0b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78b0b-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78b0b-126">Panoramica dell'architettura UPnP</span><span class="sxs-lookup"><span data-stu-id="78b0b-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="78b0b-127">Informazioni generali e background.</span><span class="sxs-lookup"><span data-stu-id="78b0b-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="78b0b-128">Panoramica sui punti di controllo</span><span class="sxs-lookup"><span data-stu-id="78b0b-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="78b0b-129">Informazioni generali sull'API del punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="78b0b-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="78b0b-130">Uso dell'API del punto di controllo</span><span class="sxs-lookup"><span data-stu-id="78b0b-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="78b0b-131">Codice di esempio che illustra come sviluppare applicazioni che controllano i dispositivi certificati UPnP.</span><span class="sxs-lookup"><span data-stu-id="78b0b-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="78b0b-132">Riferimento all'API del punto di controllo</span><span class="sxs-lookup"><span data-stu-id="78b0b-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="78b0b-133">Documentazione delle interfacce, dei metodi e degli eventi del componente del punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="78b0b-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="78b0b-134">Panoramica dell'API dell'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="78b0b-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="78b0b-135">Informazioni generali sull'API dell'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b0b-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="78b0b-136">Uso dell'API host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="78b0b-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="78b0b-137">Codice di esempio che illustra come sviluppare un'applicazione per i dispositivi certificati UPnP.</span><span class="sxs-lookup"><span data-stu-id="78b0b-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="78b0b-138">Informazioni di riferimento sull'API dell'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="78b0b-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="78b0b-139">Documentazione delle interfacce, dei metodi e degli eventi del componente host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b0b-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





