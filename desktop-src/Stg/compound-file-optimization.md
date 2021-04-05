---
title: Ottimizzazione file composto
description: L'archiviazione asincrona consente alle applicazioni di eseguire il layout preciso dei file composti, in modo che i dati siano disponibili nell'ordine in cui le applicazioni lo richiedono.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Ottimizzazione file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708200"
---
# <a name="compound-file-optimization"></a><span data-ttu-id="9fa98-104">Ottimizzazione file composto</span><span class="sxs-lookup"><span data-stu-id="9fa98-104">Compound File Optimization</span></span>

<span data-ttu-id="9fa98-105">L'archiviazione asincrona consente alle applicazioni di eseguire il layout preciso dei file composti, in modo che i dati siano disponibili nell'ordine in cui le applicazioni lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="9fa98-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="9fa98-106">Se un'applicazione richiede solo una parte dei dati per visualizzare una prima pagina di informazioni, questi dati possono essere posizionati all'inizio del file, anche se si trova logicamente alla fine di un flusso.</span><span class="sxs-lookup"><span data-stu-id="9fa98-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="9fa98-107">I dati provenienti da flussi diversi possono essere interfogliati.</span><span class="sxs-lookup"><span data-stu-id="9fa98-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="9fa98-108">I dati audio e video, ad esempio, possono essere interfogliati in modo che le operazioni di lettura successive recuperino contemporaneamente un requisito per le applicazioni multimediali.</span><span class="sxs-lookup"><span data-stu-id="9fa98-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="9fa98-109">[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) può essere utilizzato per il layout di un DocFile, migliorando così le prestazioni nella maggior parte degli scenari.</span><span class="sxs-lookup"><span data-stu-id="9fa98-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




