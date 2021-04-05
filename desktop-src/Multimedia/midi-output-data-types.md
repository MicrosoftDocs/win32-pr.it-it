---
title: Tipi di dati di output MIDI
description: Tipi di dati di output MIDI
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- MIDI (Musical Instrument Digital Interface), tipi di dati di output
- MIDI (Musical Instrument Digital Interface), tipi di dati di output
- riproduzione di file MIDI, tipi di dati di output
- Tipi di dati di output MIDI
- Tipo di dati MIDIHDR
- Tipo di dati MIDIOUTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726327"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="8de27-109">Tipi di dati di output MIDI</span><span class="sxs-lookup"><span data-stu-id="8de27-109">MIDI Output Data Types</span></span>

<span data-ttu-id="8de27-110">Windows definisce i tipi di dati seguenti per le funzioni di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="8de27-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="8de27-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8de27-111">Value</span></span>                              | <span data-ttu-id="8de27-112">Significato</span><span class="sxs-lookup"><span data-stu-id="8de27-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8de27-113">**HMIDIOUT**</span><span class="sxs-lookup"><span data-stu-id="8de27-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="8de27-114">Handle di un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="8de27-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="8de27-115">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="8de27-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="8de27-116">Intestazione per un blocco di dati di flusso o esclusivi del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="8de27-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="8de27-117">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="8de27-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="8de27-118">Struttura usata per richiedere informazioni sulle funzionalità di un particolare dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="8de27-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 