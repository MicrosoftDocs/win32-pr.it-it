---
title: Buffer audio
description: Buffer audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709178"
---
# <a name="audio-buffers"></a><span data-ttu-id="376de-107">Buffer audio</span><span class="sxs-lookup"><span data-stu-id="376de-107">Audio Buffers</span></span>

<span data-ttu-id="376de-108">È possibile controllare la parte audio di un'operazione di acquisizione in tre modi:</span><span class="sxs-lookup"><span data-stu-id="376de-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="376de-109">Includere o escludere l'audio dall'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="376de-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="376de-110">Richiedere un numero specifico di buffer audio.</span><span class="sxs-lookup"><span data-stu-id="376de-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="376de-111">Richiedere che i buffer audio siano di dimensioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="376de-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="376de-112">È possibile recuperare le impostazioni per i buffer audio usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="376de-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="376de-113">Il membro **fCaptureAudio** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) specifica se l'audio è incluso o escluso dall'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="376de-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="376de-114">Il numero di buffer audio richiesto corrente viene archiviato nel membro **wNumAudioRequested** e le dimensioni correnti del buffer audio sono archiviate nel membro **dwAudioBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="376de-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="376de-115">È possibile specificare se includere l'acquisizione audio, specificare le dimensioni e il numero di buffer audio aggiornando questi membri e inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ di serie WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="376de-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="376de-116">Per impostazione predefinita, l'audio è incluso nell'operazione di acquisizione e quattro buffer audio sono allocati.</span><span class="sxs-lookup"><span data-stu-id="376de-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="376de-117">Il valore predefinito di **fCaptureAudio** è **true**.</span><span class="sxs-lookup"><span data-stu-id="376de-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="376de-118">Le dimensioni predefinite del buffer (il valore di **dwAudioBufferSize**) possono contenere 0,5 secondi di dati audio o 10.000, a seconda del valore maggiore.</span><span class="sxs-lookup"><span data-stu-id="376de-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




