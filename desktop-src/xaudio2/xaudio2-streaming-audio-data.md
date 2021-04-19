---
description: Il flusso è il processo di gestione di una piccola parte di un file audio in memoria. Ciò consente di riprodurre file audio di grandi dimensioni, ad esempio la musica in background, e di non richiedere una grande quantità di memoria.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Dati audio di streaming XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317840"
---
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="eb12c-104">Dati audio di streaming XAudio2</span><span class="sxs-lookup"><span data-stu-id="eb12c-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="eb12c-105">Il flusso è il processo di gestione di una piccola parte di un file audio in memoria.</span><span class="sxs-lookup"><span data-stu-id="eb12c-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="eb12c-106">Ciò consente di riprodurre file audio di grandi dimensioni, ad esempio la musica in background, e di non richiedere una grande quantità di memoria.</span><span class="sxs-lookup"><span data-stu-id="eb12c-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="eb12c-107">Quando si esegue il flusso di un file audio, i relativi dati vengono letti dal disco in blocchi anziché caricare l'intero file in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="eb12c-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="eb12c-108">Il flusso viene eseguito in modo asincrono leggendo i dati audio in una coda di buffer del disco.</span><span class="sxs-lookup"><span data-stu-id="eb12c-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="eb12c-109">Ogni buffer viene riempito e quindi inviato a una voce di origine.</span><span class="sxs-lookup"><span data-stu-id="eb12c-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="eb12c-110">Quando la voce termina la riproduzione di un buffer, il buffer diventa disponibile per la lettura.</span><span class="sxs-lookup"><span data-stu-id="eb12c-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="eb12c-111">Il ciclo dei buffer del disco in questo modo consente di riprodurre un file audio di grandi dimensioni mentre viene caricata solo una parte dei dati.</span><span class="sxs-lookup"><span data-stu-id="eb12c-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="eb12c-112">Il codice di streaming deve essere inserito in un thread separato, in cui può essere sospeso durante l'attesa del completamento delle operazioni di disco e audio con esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="eb12c-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="eb12c-113">Una classe di callback viene utilizzata per riattivare il thread attivando gli eventi quando le operazioni audio sono state completate.</span><span class="sxs-lookup"><span data-stu-id="eb12c-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="eb12c-114">Per un esempio di come è possibile eseguire lo streaming con XAudio2, vedere [procedura: trasmettere un suono dal disco](how-to--stream-a-sound-from-disk.md).</span><span class="sxs-lookup"><span data-stu-id="eb12c-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb12c-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb12c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb12c-116">Streaming di dati audio</span><span class="sxs-lookup"><span data-stu-id="eb12c-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="eb12c-117">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="eb12c-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



