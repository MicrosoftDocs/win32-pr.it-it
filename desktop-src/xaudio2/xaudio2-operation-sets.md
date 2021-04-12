---
description: Questa panoramica introduce diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Set di operazioni XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234057"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="af44e-103">Set di operazioni XAudio2</span><span class="sxs-lookup"><span data-stu-id="af44e-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="af44e-104">Questa panoramica introduce diversi metodi XAudio2 che è possibile chiamare come parte di un set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="af44e-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="af44e-105">Diversi metodi XAudio2 accettano l'argomento *operationt* , che consente di chiamarli come parte di un gruppo posticipato.</span><span class="sxs-lookup"><span data-stu-id="af44e-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="af44e-106">A un momento specifico, è possibile applicare un intero set di modifiche contemporaneamente chiamando la funzione [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con l'identificatore del set di *operazioni* per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="af44e-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="af44e-107">L'identificatore è un numero arbitrario.</span><span class="sxs-lookup"><span data-stu-id="af44e-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="af44e-108">Consente quindi a parti separate del codice client di applicare modifiche atomiche separate al grafo senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="af44e-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="af44e-109">La procedura consigliata consiste nel fare in modo che il client incrementi un contatore globale ogni volta che è necessario generare un identificatore univoco di un nuovo *operatore* .</span><span class="sxs-lookup"><span data-stu-id="af44e-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="af44e-110">Un set di modifiche apportate al grafo, applicato in modo atomico, è sicuramente accurato.</span><span class="sxs-lookup"><span data-stu-id="af44e-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="af44e-111">Ad esempio, le voci vengono avviate sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="af44e-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="af44e-112">Se si imposta *Operational* su XAUDIO2 \_ commit \_ Now, la modifica viene applicata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="af44e-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="af44e-113">Viene applicata nel primo passaggio di elaborazione audio dopo la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="af44e-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="af44e-114">Se si chiama [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con XAUDIO2 \_ commit \_ All, verranno eseguite le modifiche apportate a tutti i set di operazioni in sospeso, indipendentemente dall'identificatore del set di *operazioni* .</span><span class="sxs-lookup"><span data-stu-id="af44e-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="af44e-115">Determinati metodi hanno effetto immediatamente quando vengono chiamati da un callback XAudio2 con un *operatore* di XAudio2 \_ commit \_ Now.</span><span class="sxs-lookup"><span data-stu-id="af44e-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="af44e-116">Tutti gli altri metodi che accettano un argomento di *operationst* hanno effetto solo sul successivo passaggio di elaborazione dopo che il metodo è stato chiamato (se chiamato con XAUDIO2 \_ commit \_ Now) o dopo la chiamata di [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con lo stesso *operatore*.</span><span class="sxs-lookup"><span data-stu-id="af44e-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="af44e-117">Per questo motivo, alcune chiamate al metodo potrebbero non essere sempre eseguite nello stesso ordine in cui sono state chiamate.</span><span class="sxs-lookup"><span data-stu-id="af44e-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="af44e-118">Tutte le operazioni in sospeso vengono sottoposte a commit in modo atomico quando viene chiamato [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) .</span><span class="sxs-lookup"><span data-stu-id="af44e-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="af44e-119">Tutti i metodi che vengono chiamati mentre il motore viene arrestato diventano immediatamente effettivi, indipendentemente dal valore di *operationt* fornito.</span><span class="sxs-lookup"><span data-stu-id="af44e-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="af44e-120">Quando si riavvia il motore, XAudio2 torna alla modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="af44e-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="af44e-121">Gli scenari semplici in cui i set di operazioni sono utili includono gli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="af44e-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="af44e-122">Avvio simultaneo di più voci.</span><span class="sxs-lookup"><span data-stu-id="af44e-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="af44e-123">Inviando contemporaneamente un buffer a una voce, impostando i parametri vocali e avviando la voce.</span><span class="sxs-lookup"><span data-stu-id="af44e-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="af44e-124">Creazione di una modifica su larga scala nel grafico, ad esempio la connessione di tutte le voci di origine a una nuova voce submix.</span><span class="sxs-lookup"><span data-stu-id="af44e-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="af44e-125">Per un esempio di utilizzo di un set di operazioni, vedere [procedura: raggruppare i metodi audio come set di operazioni](how-to--group-audio-methods-as-an-operation-set.md) .</span><span class="sxs-lookup"><span data-stu-id="af44e-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="af44e-126">Metodi del set di operazioni</span><span class="sxs-lookup"><span data-stu-id="af44e-126">Operation Set Methods</span></span>

<span data-ttu-id="af44e-127">È possibile chiamare i metodi seguenti come parte di un set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="af44e-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="af44e-128">**IXAudio2SourceVoice::ExitLoop**</span><span class="sxs-lookup"><span data-stu-id="af44e-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="af44e-129">**IXAudio2Voice::SetFilterParameters**</span><span class="sxs-lookup"><span data-stu-id="af44e-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="af44e-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span><span class="sxs-lookup"><span data-stu-id="af44e-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="af44e-131">**IXAudio2Voice::D isableEffect**</span><span class="sxs-lookup"><span data-stu-id="af44e-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="af44e-132">**IXAudio2Voice::EnableEffect**</span><span class="sxs-lookup"><span data-stu-id="af44e-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="af44e-133">**IXAudio2Voice::SetChannelVolumes**</span><span class="sxs-lookup"><span data-stu-id="af44e-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="af44e-134">**IXAudio2Voice::SetEffectParameters**</span><span class="sxs-lookup"><span data-stu-id="af44e-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="af44e-135">**IXAudio2Voice::SetOutputMatrix**</span><span class="sxs-lookup"><span data-stu-id="af44e-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="af44e-136">**IXAudio2Voice:: sevolume**</span><span class="sxs-lookup"><span data-stu-id="af44e-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="af44e-137">**IXAudio2SourceVoice:: Start**</span><span class="sxs-lookup"><span data-stu-id="af44e-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="af44e-138">**IXAudio2SourceVoice:: Stop**</span><span class="sxs-lookup"><span data-stu-id="af44e-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="af44e-139">Come descritto in precedenza, il codice client deve infine chiamare la funzione [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) per eseguire le modifiche posticipate.</span><span class="sxs-lookup"><span data-stu-id="af44e-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af44e-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af44e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af44e-141">Set di operazioni</span><span class="sxs-lookup"><span data-stu-id="af44e-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="af44e-142">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="af44e-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="af44e-143">Procedura: Raggruppare metodi audio come set di operazioni</span><span class="sxs-lookup"><span data-stu-id="af44e-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
