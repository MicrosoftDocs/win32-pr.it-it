---
description: Enumerazioni audio principali
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Enumerazioni audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483917"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="26e5d-103">Enumerazioni audio principali</span><span class="sxs-lookup"><span data-stu-id="26e5d-103">Core Audio Enumerations</span></span>

<span data-ttu-id="26e5d-104">In questa sezione vengono descritte le enumerazioni utilizzate dalle API di base audio in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="26e5d-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="26e5d-105">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="26e5d-105">Enumeration</span></span>                                                                   | <span data-ttu-id="26e5d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26e5d-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26e5d-107">**\_\_BUFFERFLAGS AUDCLNT**</span><span class="sxs-lookup"><span data-stu-id="26e5d-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="26e5d-108">Flag di stato per un buffer dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="26e5d-109">**\_SHAREMODE AUDCLNT**</span><span class="sxs-lookup"><span data-stu-id="26e5d-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="26e5d-110">Modalità di condivisione per un flusso.</span><span class="sxs-lookup"><span data-stu-id="26e5d-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="26e5d-111">**\_STREAMOPTIONS AUDCLNT**</span><span class="sxs-lookup"><span data-stu-id="26e5d-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="26e5d-112">Definisce i valori che descrivono le caratteristiche di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="26e5d-113">**\_categoria flusso \_ audio**</span><span class="sxs-lookup"><span data-stu-id="26e5d-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="26e5d-114">Specifica la categoria di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="26e5d-115">**AudioSessionState**</span><span class="sxs-lookup"><span data-stu-id="26e5d-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="26e5d-116">Stato di una sessione audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="26e5d-117">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="26e5d-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="26e5d-118">Tipo di connettore in una topologia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26e5d-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="26e5d-119">**DataFlow**</span><span class="sxs-lookup"><span data-stu-id="26e5d-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="26e5d-120">Direzione del flusso di dati di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="26e5d-121">**EDataFlow**</span><span class="sxs-lookup"><span data-stu-id="26e5d-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="26e5d-122">Direzione di flusso dei dati audio tra un dispositivo endpoint audio e un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="26e5d-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="26e5d-123">**EndpointFormFactor**</span><span class="sxs-lookup"><span data-stu-id="26e5d-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="26e5d-124">Attributi fisici generali di un dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="26e5d-125">**ERole**</span><span class="sxs-lookup"><span data-stu-id="26e5d-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="26e5d-126">Ruolo del sistema di un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="26e5d-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="26e5d-127">**\_CONNECTIONTYPE sink \_ KSJACK**</span><span class="sxs-lookup"><span data-stu-id="26e5d-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="26e5d-128">Tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="26e5d-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="26e5d-129">**PartType**</span><span class="sxs-lookup"><span data-stu-id="26e5d-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="26e5d-130">Il tipo di parte di una parte (connettore o unità secondaria) in una topologia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26e5d-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="26e5d-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26e5d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26e5d-132">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="26e5d-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




