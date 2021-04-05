---
title: Informazioni sui gestori di file e flussi personalizzati
description: Informazioni sui gestori di file e flussi personalizzati
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video per Windows (VFW), gestori di file personalizzati
- Video per Windows (VFW), gestori di flussi personalizzati
- Video per Windows (VFW), gestori di file
- Video per Windows (VFW), gestori di flusso
- VFW (video per Windows), gestori di file personalizzati
- VFW (video per Windows), gestori di flussi personalizzati
- VFW (video per Windows), gestori di file
- VFW (video per Windows), gestori di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856917"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="5b234-111">Informazioni sui gestori di file e flussi personalizzati</span><span class="sxs-lookup"><span data-stu-id="5b234-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="5b234-112">L'applicazione può usare un gestore di file personalizzato per leggere da un file o scrivere in un file in un formato non standard.</span><span class="sxs-lookup"><span data-stu-id="5b234-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="5b234-113">A tale scopo, l'applicazione usa semplicemente il nome del gestore di file quando si apre il file o si alloca l'interfaccia del file.</span><span class="sxs-lookup"><span data-stu-id="5b234-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="5b234-114">La libreria AVIFile usa quindi le funzioni del gestore di file anziché quelle di un altro gestore di file.</span><span class="sxs-lookup"><span data-stu-id="5b234-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="5b234-115">Il formato non standard viene visualizzato come dati AVI standard nell'applicazione o in qualsiasi altra applicazione che usa il gestore di file personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5b234-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="5b234-116">Analogamente, l'applicazione può usare un gestore di flusso personalizzato per leggere un flusso in un formato non standard.</span><span class="sxs-lookup"><span data-stu-id="5b234-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="5b234-117">Un flusso, indipendentemente dal fatto che sia costituito da dati audio, video, MIDI, testo o personalizzati, è un componente di un file AVI.</span><span class="sxs-lookup"><span data-stu-id="5b234-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="5b234-118">Ad esempio, un file AVI che contiene una sequenza video, una colonna inglese e una colonna musicale francese è costituito da tre flussi.</span><span class="sxs-lookup"><span data-stu-id="5b234-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="5b234-119">L'applicazione può specificare i flussi in un file AVI per elaborare e indirizzare ognuno di questi flussi a un gestore che può elaborare in modo ottimale il tipo di dati multimediali appropriato.</span><span class="sxs-lookup"><span data-stu-id="5b234-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="5b234-120">È necessario inserire gestori di file e di flusso personalizzati in una o più dll, separate dai file dell'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="5b234-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




