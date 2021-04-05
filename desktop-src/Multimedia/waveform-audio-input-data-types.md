---
title: Tipi di dati di input Waveform-Audio
description: Tipi di dati di input Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio Waveform, tipi di dati di input
- waveform-interfaccia audio, tipi di dati di input
- registrazione audio della forma d'onda, tipi di dati di input
- Handle HWAVEIN
- Struttura WAVEFORMATEX
- Struttura WAVEHDR
- Struttura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046675"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="f1c5e-110">Tipi di dati di input Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="f1c5e-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="f1c5e-111">I tipi di dati seguenti sono definiti per le funzioni di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="f1c5e-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1c5e-112">Type</span></span>                                 | <span data-ttu-id="f1c5e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1c5e-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c5e-114">**HWAVEIN**</span><span class="sxs-lookup"><span data-stu-id="f1c5e-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="f1c5e-115">Handle di un dispositivo di input audio e di forma d'onda aperto.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="f1c5e-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f1c5e-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="f1c5e-117">Struttura che specifica i formati di dati supportati da un dispositivo di input audio e di forma d'onda particolare.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="f1c5e-118">Questa struttura viene usata anche per i dispositivi di output dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="f1c5e-119">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="f1c5e-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="f1c5e-120">Struttura utilizzata come intestazione per un blocco di dati di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="f1c5e-121">Questa struttura viene usata anche per i dispositivi di output dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="f1c5e-122">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="f1c5e-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="f1c5e-123">Struttura usata per richiedere informazioni sulle funzionalità di un dispositivo di input audio e di forma d'onda particolare.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="f1c5e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1c5e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c5e-125">Registrazione dell'audio della forma d'onda</span><span class="sxs-lookup"><span data-stu-id="f1c5e-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 