---
description: Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233714"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="c6964-103">Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c6964-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="c6964-104">In rari scenari, è opportuno sincronizzare con precisione il rendering video con la frequenza di aggiornamento del monitoraggio, in modo che ogni volta che il monitoraggio venga aggiornato viene visualizzato esattamente un nuovo frame.</span><span class="sxs-lookup"><span data-stu-id="c6964-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="c6964-105">Il modo più affidabile per eseguire questa operazione consiste nel creare un allocatore-Presenter personalizzato che usa un'operazione di capovolgimento anziché un'operazione blit per scrivere i bit video nell'area primaria.</span><span class="sxs-lookup"><span data-stu-id="c6964-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="c6964-106">"Flip" viene chiamato ogni volta che il monitoraggio viene aggiornato, quindi se il flusso video non contiene timestamp, il VMR viene eseguito il rendering il più rapidamente possibile nell'area primaria, ma la superficie bloccherà il flusso fino al completamento dell'operazione di capovolgimento.</span><span class="sxs-lookup"><span data-stu-id="c6964-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="c6964-107">Ciò significa che, finché la CPU non è sovraccarica, il fotogramma successivo sarà sempre in attesa nella superficie primaria ogni volta che il monitoraggio viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c6964-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="c6964-108">Tuttavia, se è in esecuzione un altro processo con utilizzo intensivo della CPU, è possibile che il thread di streaming DirectShow muoia in modo improprio, in modo che non sia in grado di recapitare i frame video in modo sufficientemente rapido</span><span class="sxs-lookup"><span data-stu-id="c6964-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6964-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6964-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6964-110">Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)</span><span class="sxs-lookup"><span data-stu-id="c6964-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



