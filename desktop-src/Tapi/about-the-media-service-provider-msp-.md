---
description: Un provider di servizi multimediali (MSP) TAPI 3 consente a un'applicazione di controllare in modo significativo i supporti per un meccanismo di trasporto specifico.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Informazioni sul provider di servizi multimediali (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132154"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="cca0c-103">Informazioni sul provider di servizi multimediali (MSP)</span><span class="sxs-lookup"><span data-stu-id="cca0c-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="cca0c-104">Un provider di servizi multimediali (MSP) TAPI 3 consente a un'applicazione di controllare in modo significativo i supporti per un meccanismo di trasporto specifico.</span><span class="sxs-lookup"><span data-stu-id="cca0c-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="cca0c-105">Un MSP esiste sempre abbinato a un provider di servizi di telefonia (TSP).</span><span class="sxs-lookup"><span data-stu-id="cca0c-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="cca0c-106">Proprio come un TSP è un livello di astrazione per il controllo delle chiamate, MSP controlla i supporti senza necessità di codifica specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cca0c-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="cca0c-107">Per un esempio di comunicazione MSP/TSP, vedere [Panoramica del provider di servizi TAPI](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cca0c-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="cca0c-108">Un MSP Abilita il controllo multimediale attraverso l'uso di interfacce speciali di Terminal, flusso e sottoflusso definite da TAPI.</span><span class="sxs-lookup"><span data-stu-id="cca0c-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="cca0c-109">Il diagramma in [informazioni sui controlli Call e media](about-call-and-media-controls.md) illustra il modo in cui queste interfacce vengono visualizzate in un'applicazione TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="cca0c-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="cca0c-110">Inoltre, un MSP può implementare interfacce private [specifiche del provider](provider-specific-interfaces.md), che TAPI si aggregano sugli oggetti standard esposti a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cca0c-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="cca0c-111">Ad esempio, Microsoft IPConf MSP, installato con Microsoft Windows 2000, implementa l'interfaccia [**ITParticipant**](itparticipant.md) , che fornisce i controlli per i singoli membri di una conferenza.</span><span class="sxs-lookup"><span data-stu-id="cca0c-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="cca0c-112">Nell'argomento seguente viene brevemente descritto il MSPs che può essere installato con un sistema operativo Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cca0c-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="cca0c-113">Per informazioni dettagliate sulla configurazione e sull'utilizzo, vedere Resource Kit per la piattaforma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cca0c-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="cca0c-114">È possibile scrivere altri provider di servizi multimediali di terze parti per i protocolli specifici o per i dispositivi fisici.</span><span class="sxs-lookup"><span data-stu-id="cca0c-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="cca0c-115">[Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) descrive le interfacce che devono essere implementate per consentire a un MSP di interagire con i componenti della telefonia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cca0c-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 
