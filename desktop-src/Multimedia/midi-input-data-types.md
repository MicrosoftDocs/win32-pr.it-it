---
title: Tipi di dati di input MIDI
description: Tipi di dati di input MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- MIDI (Musical Instrument Digital Interface), tipi di dati di input
- MIDI (Musical Instrument Digital Interface), tipi di dati di input
- registrazione audio MIDI, tipi di dati di input
- Tipi di dati di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299750"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="e981d-107">Tipi di dati di input MIDI</span><span class="sxs-lookup"><span data-stu-id="e981d-107">MIDI Input Data Types</span></span>

<span data-ttu-id="e981d-108">Windows definisce i tipi di dati seguenti per le funzioni di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="e981d-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="e981d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="e981d-109">Value</span></span>                            | <span data-ttu-id="e981d-110">Significato</span><span class="sxs-lookup"><span data-stu-id="e981d-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e981d-111">**HMIDIIN**</span><span class="sxs-lookup"><span data-stu-id="e981d-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="e981d-112">Handle di un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="e981d-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="e981d-113">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="e981d-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="e981d-114">Intestazione per un buffer di flusso o un blocco di dati esclusivi del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="e981d-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="e981d-115">Per le applicazioni di input, questa struttura registra solo i dati esclusivi del sistema (il flusso non è supportato per l'input MIDI).</span><span class="sxs-lookup"><span data-stu-id="e981d-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="e981d-116">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="e981d-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="e981d-117">Struttura usata per richiedere informazioni sulle funzionalità di un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="e981d-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e981d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e981d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e981d-119">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="e981d-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 