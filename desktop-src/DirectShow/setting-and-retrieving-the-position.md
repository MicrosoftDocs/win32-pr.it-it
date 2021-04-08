---
description: Impostazione e recupero della posizione
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Impostazione e recupero della posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745410"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="62557-103">Impostazione e recupero della posizione</span><span class="sxs-lookup"><span data-stu-id="62557-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="62557-104">Il grafico del filtro mantiene due valori di posizione, la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="62557-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="62557-105">Questi vengono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="62557-105">These are defined as follows:</span></span>

-   <span data-ttu-id="62557-106">Quando il grafico è in esecuzione, la posizione corrente è la posizione di riproduzione corrente, relativa all'inizio dell'origine.</span><span class="sxs-lookup"><span data-stu-id="62557-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="62557-107">Quando il grafico viene arrestato o sospeso, la posizione corrente è il punto in cui verrà avviato il flusso al successivo comando di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="62557-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="62557-108">La posizione di arresto è il punto in cui si concluderà il flusso.</span><span class="sxs-lookup"><span data-stu-id="62557-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="62557-109">Quando il grafico raggiunge la posizione di arresto, non viene eseguito il flusso di più dati e il gestore del grafo del filtro pubblica un evento di [**\_ completamento EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="62557-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="62557-110">Tuttavia, il grafico non passa automaticamente allo stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="62557-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="62557-111">Per ulteriori informazioni, vedere [risposta agli eventi](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="62557-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="62557-112">Per recuperare questi valori, chiamare il metodo [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="62557-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="62557-113">I valori restituiti sono sempre relativi all'origine del supporto originale.</span><span class="sxs-lookup"><span data-stu-id="62557-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="62557-114">Per impostazione predefinita, i valori sono in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="62557-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="62557-115">In alcuni casi, è possibile modificare le unità di tempo; per altre informazioni, vedere [formati di ora per i comandi Seek](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="62557-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="62557-116">Per cercare una nuova posizione o impostare una nuova posizione di arresto, chiamare il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="62557-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="62557-117">Un secondo è 10 milioni unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="62557-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="62557-118">Per praticità, l'esempio definisce questo valore come un \_ secondo.</span><span class="sxs-lookup"><span data-stu-id="62557-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="62557-119">Se si usa la libreria di classi base DirectShow, le unità di costante hanno lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="62557-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="62557-120">Il parametro *rtNow* specifica la nuova posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="62557-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="62557-121">Il secondo parametro è un flag che definisce come interpretare *rtNow*.</span><span class="sxs-lookup"><span data-stu-id="62557-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="62557-122">In questo esempio il flag AM \_ seeking \_ AbsolutePositioning indica che *rtNow* specifica una posizione assoluta nell'origine.</span><span class="sxs-lookup"><span data-stu-id="62557-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="62557-123">Il grafico del filtro cercherà quindi una posizione di due secondi dall'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="62557-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="62557-124">Il parametro *rtStop* restituisce l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="62557-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="62557-125">L'ultimo parametro specifica che *rtStop* è anche una posizione assoluta.</span><span class="sxs-lookup"><span data-stu-id="62557-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="62557-126">Per specificare una posizione rispetto al valore di posizione precedente, usare il \_ \_ flag RelativePositioning seeking.</span><span class="sxs-lookup"><span data-stu-id="62557-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="62557-127">Per lasciare invariato uno dei valori di posizione, utilizzare il \_ \_ flag nopositioning am seeking.</span><span class="sxs-lookup"><span data-stu-id="62557-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="62557-128">Il parametro time corrispondente può essere **null** in questo caso.</span><span class="sxs-lookup"><span data-stu-id="62557-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="62557-129">L'esempio seguente cerca di 10 secondi, ma lascia invariata la posizione di arresto:</span><span class="sxs-lookup"><span data-stu-id="62557-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="62557-130">Se il grafico del filtro viene arrestato, il renderer video non aggiorna l'immagine dopo un'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="62557-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="62557-131">L'utente verrà visualizzato come se la ricerca non venisse eseguita.</span><span class="sxs-lookup"><span data-stu-id="62557-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="62557-132">Per aggiornare l'immagine, sospendere il grafico dopo l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="62557-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="62557-133">La sospensione del grafico è un nuovo fotogramma video per il renderer video.</span><span class="sxs-lookup"><span data-stu-id="62557-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="62557-134">È possibile usare il metodo [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , che sospende il grafico e lo arresta.</span><span class="sxs-lookup"><span data-stu-id="62557-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



