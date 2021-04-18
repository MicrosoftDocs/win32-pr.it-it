---
description: Esempio di filtro metronomo
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Esempio di filtro metronomo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303993"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="de933-103">Esempio di filtro metronomo</span><span class="sxs-lookup"><span data-stu-id="de933-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="de933-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de933-104">Description</span></span>

<span data-ttu-id="de933-105">Questo filtro di esempio Mostra come implementare un orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="de933-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="de933-106">Il filtro usa l'input del microfono predefinito per ascoltare i picchi audio (ad esempio clic, applausi delle mani o tosse), che usa per determinare una frequenza di clock.</span><span class="sxs-lookup"><span data-stu-id="de933-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="de933-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="de933-107">Usage</span></span>

<span data-ttu-id="de933-108">Compilare il progetto di esempio e copiare la DLL di filtro (Metronom.ax) nella directory di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="de933-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="de933-109">Eseguire il file Metronom. reg per registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="de933-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="de933-110">Per utilizzare il filtro:</span><span class="sxs-lookup"><span data-stu-id="de933-110">To use the filter:</span></span>

1.  <span data-ttu-id="de933-111">Creare un grafico di filtro in GraphEdit che esegue il rendering di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="de933-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="de933-112">Elimina tutti i flussi audio sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="de933-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="de933-113">Aggiungere il filtro Metronome al grafico.</span><span class="sxs-lookup"><span data-stu-id="de933-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="de933-114">Viene visualizzato nella categoria filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="de933-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="de933-115">Eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="de933-115">Run the graph.</span></span> <span data-ttu-id="de933-116">Il video inizierà a giocare alla velocità normale.</span><span class="sxs-lookup"><span data-stu-id="de933-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="de933-117">Battere le mani o usare un metronomo per impostare una nuova velocità.</span><span class="sxs-lookup"><span data-stu-id="de933-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="de933-118">Note sulla programmazione</span><span class="sxs-lookup"><span data-stu-id="de933-118">Programming Notes</span></span>

<span data-ttu-id="de933-119">Questo filtro funziona solo per i video.</span><span class="sxs-lookup"><span data-stu-id="de933-119">This filter works only for video.</span></span> <span data-ttu-id="de933-120">Il renderer audio non è in grado di eseguire la sincronizzazione con frequenze di clock radicalmente differenti.</span><span class="sxs-lookup"><span data-stu-id="de933-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="de933-121">Se si applaude 92 volte al minuto (una volta ogni ~ 652 MS), il video viene riprodotto alla tariffa normale.</span><span class="sxs-lookup"><span data-stu-id="de933-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="de933-122">È possibile modificare questa impostazione predefinita modificando il valore della costante `BPM` in Metronom. cpp.</span><span class="sxs-lookup"><span data-stu-id="de933-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="de933-123">Se si smette di applaudire per un certo periodo di tempo e quindi si inizia di nuovo a applaudire, è necessario ricominciare approssimativamente la stessa velocità oppure il filtro lo ignorerà.</span><span class="sxs-lookup"><span data-stu-id="de933-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="de933-124">Inoltre, la velocità di riproduzione del video è limitata dalla velocità della CPU.</span><span class="sxs-lookup"><span data-stu-id="de933-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="de933-125">Se si supera il limite per un determinato periodo di tempo, il filtro smetterà di rispondere alle modifiche di frequenza.</span><span class="sxs-lookup"><span data-stu-id="de933-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="de933-126">In questo caso, arrestare il grafo e riavviare.</span><span class="sxs-lookup"><span data-stu-id="de933-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="de933-127">Se si implementa un orologio personalizzato, le regole più importanti sono che gli orologi di riferimento non devono tornare indietro.</span><span class="sxs-lookup"><span data-stu-id="de933-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="de933-128">Ovvero non devono mai segnalare un valore di ora minore del valore di ora precedente.</span><span class="sxs-lookup"><span data-stu-id="de933-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="de933-129">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de933-129">Downloading the Sample</span></span>

<span data-ttu-id="de933-130">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de933-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="de933-131">Questo esempio viene installato nel seguente percorso: *\[ SDK radice \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Metronome.</span><span class="sxs-lookup"><span data-stu-id="de933-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de933-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de933-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de933-133">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="de933-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="de933-134">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="de933-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



