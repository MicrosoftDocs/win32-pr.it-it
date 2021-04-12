---
title: Formato del buffer del flusso
description: Formato del buffer del flusso
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- buffer di flusso, formato
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398854"
---
# <a name="stream-buffer-format"></a><span data-ttu-id="65ca2-108">Formato del buffer del flusso</span><span class="sxs-lookup"><span data-stu-id="65ca2-108">Stream Buffer Format</span></span>

<span data-ttu-id="65ca2-109">Il membro **lpData** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) punta a un buffer del flusso e il membro **dwBufferLength** specifica le dimensioni effettive del buffer.</span><span class="sxs-lookup"><span data-stu-id="65ca2-109">The **lpData** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure points to a stream buffer, and the **dwBufferLength** member specifies the actual size of this buffer.</span></span> <span data-ttu-id="65ca2-110">Il membro **dwBytesRecorded** di **MIDIHDR** specifica il numero di byte nel buffer usati effettivamente dagli eventi MIDI; Questo valore deve essere minore o uguale al valore specificato da **dwBufferLength**.</span><span class="sxs-lookup"><span data-stu-id="65ca2-110">The **dwBytesRecorded** member of **MIDIHDR** specifies the number of bytes in the buffer that are actually used by the MIDI events; this value must be less than or equal to the value specified by **dwBufferLength**.</span></span>

<span data-ttu-id="65ca2-111">Ogni evento MIDI nel buffer del flusso viene specificato da una struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , che contiene l'ora per l'evento, un identificatore di flusso, un codice evento e, quando appropriato, i parametri per l'evento.</span><span class="sxs-lookup"><span data-stu-id="65ca2-111">Each of the MIDI events in the stream buffer is specified by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure, which contains the time for the event, a stream identifier, an event code, and, when appropriate, parameters for the event.</span></span> <span data-ttu-id="65ca2-112">Ognuna di queste strutture **MIDIEVENT** deve iniziare con un limite di parola doppia.</span><span class="sxs-lookup"><span data-stu-id="65ca2-112">Each of these **MIDIEVENT** structures must begin on a doubleword boundary.</span></span> <span data-ttu-id="65ca2-113">Se necessario, i byte di riempimento devono essere aggiunti alla fine della struttura per garantire che il successivo venga avviato su un limite di parola doppia.</span><span class="sxs-lookup"><span data-stu-id="65ca2-113">If necessary, pad bytes must be added to the end of the structure to ensure that the next one starts on a doubleword boundary.</span></span>

 

 