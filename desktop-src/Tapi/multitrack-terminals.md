---
description: TAPI 3,1 introduce la nozione di un terminale multitraccia, un terminale che, in sostanza, è una raccolta di &\# 0034, track&\# 0034; terminali.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308291"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="9143b-103">Terminali multitraccia</span><span class="sxs-lookup"><span data-stu-id="9143b-103">Multitrack Terminals</span></span>

<span data-ttu-id="9143b-104">TAPI 3,1 introduce la nozione di un terminale multitraccia, un terminale che, in sostanza, è una raccolta di terminali "Track".</span><span class="sxs-lookup"><span data-stu-id="9143b-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="9143b-105">I terminali multitraccia facilitano il caricamento del programmatore in situazioni in cui più flussi multimediali sono interessati da una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="9143b-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="9143b-106">Il [terminale di registrazione file](file-playback-terminal-and-file-recording-terminal.md) è un esempio di terminale multitraccia.</span><span class="sxs-lookup"><span data-stu-id="9143b-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="9143b-107">È costituito da "tracks", dove ogni "Track" è un terminale corrispondente a un flusso nel file registrato.</span><span class="sxs-lookup"><span data-stu-id="9143b-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="9143b-108">Un [terminale di Track](track-terminals.md) può essere un altro terminale multitraccia o un terminale a traccia singola.</span><span class="sxs-lookup"><span data-stu-id="9143b-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="9143b-109">Un terminale a traccia singola è un terminale senza terminali di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="9143b-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="9143b-110">Un terminale a traccia singola è un terminale in TAPI 3 Sense of the Word.</span><span class="sxs-lookup"><span data-stu-id="9143b-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="9143b-111">Per ulteriori informazioni sui terminali multitraccia, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9143b-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="9143b-112">Informazioni sui terminali multitraccia</span><span class="sxs-lookup"><span data-stu-id="9143b-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="9143b-113">Meccanismo di selezione terminali predefinito</span><span class="sxs-lookup"><span data-stu-id="9143b-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="9143b-114">Selezione terminale manuale</span><span class="sxs-lookup"><span data-stu-id="9143b-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="9143b-115">Uso di terminali multitraccia e del meccanismo di selezione predefinito</span><span class="sxs-lookup"><span data-stu-id="9143b-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



