---
title: Informazioni di riferimento sull'API Servizi Desktop remoto AudioEndpoint
description: Supporta le interfacce per la registrazione di endpoint audio e il trasporto di dati.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, informazioni di riferimento sull'API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396483"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="d3ee5-104">Informazioni di riferimento sull'API Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ee5-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="d3ee5-105">Un *endpoint audio* rappresenta un dispositivo audio, un'API audio o qualsiasi altra origine o sink audio e viene usato per inviare o utilizzare dati dal motore audio.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="d3ee5-106">Un endpoint audio deve essere connesso al motore audio tramite una *connessione* e a ogni connessione può essere connesso un solo endpoint.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="d3ee5-107">Dopo la registrazione di un endpoint, il motore audio connette l'endpoint alla connessione.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="d3ee5-108">Ogni oggetto endpoint deve implementare le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3ee5-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="d3ee5-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) per abilitare il motore audio per ottenere informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="d3ee5-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) per ottenere informazioni sul buffer di dati prima di eseguire un passaggio di elaborazione e inviare una notifica all'endpoint al termine del passaggio.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="d3ee5-111">Interfaccia [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , a seconda che l'oggetto endpoint stia acquisendo o eseguendo il rendering dell'audio.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="d3ee5-112">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="d3ee5-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="d3ee5-113">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="d3ee5-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="d3ee5-114">Il motore audio utilizza queste interfacce per ottenere informazioni sugli endpoint collegati al motore.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="d3ee5-115">L'implementazione dell'endpoint deve fornire il meccanismo per il recapito o l'utilizzo di dati dal motore in base a quanto specificato da tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="d3ee5-116">L'API Servizi Desktop remoto AudioEndpoint supporta i tipi di enumerazione, le interfacce e le strutture.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3ee5-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d3ee5-117">In this section</span></span>

-   [<span data-ttu-id="d3ee5-118">Tipi di enumerazione Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ee5-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="d3ee5-119">Funzioni di Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ee5-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="d3ee5-120">Interfacce di Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ee5-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="d3ee5-121">Servizi Desktop remoto strutture AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ee5-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="d3ee5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3ee5-122">Remarks</span></span>

<span data-ttu-id="d3ee5-123">L'API Servizi Desktop remoto AudioEndpoint è destinata all'uso in scenari Desktop remoto; non è per le applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="d3ee5-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




