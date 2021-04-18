---
description: Come eseguire lo scrubbing
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Come eseguire lo scrubbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527685"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="8dfce-103">Come eseguire lo scrubbing</span><span class="sxs-lookup"><span data-stu-id="8dfce-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="8dfce-104">Viene eseguita la ripulitura per cercare istantaneamente punti specifici all'interno di un file interagendo con una rappresentazione visiva del tempo, ad esempio una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="8dfce-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="8dfce-105">In Media Foundation, lo scrubbing significa cercare su un file e ottenere un frame aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8dfce-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="8dfce-106">Per informazioni sullo scrubbing, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="8dfce-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="8dfce-107">Per eseguire lo scrubbing</span><span class="sxs-lookup"><span data-stu-id="8dfce-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="8dfce-108">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dalla [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="8dfce-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8dfce-109">Non ottenere l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8dfce-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="8dfce-110">Ottenere sempre l'interfaccia dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="8dfce-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="8dfce-111">Chiamare [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) per impostare la velocità di riproduzione su zero.</span><span class="sxs-lookup"><span data-stu-id="8dfce-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="8dfce-112">Per ulteriori informazioni sulla chiamata a questo metodo, vedere [come impostare la velocità di riproduzione nella sessione multimediale](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="8dfce-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="8dfce-113">Creare una posizione di ricerca in un **PROPVARIANT** specificando il tempo di presentazione da cercare in un tipo **MFTIME** .</span><span class="sxs-lookup"><span data-stu-id="8dfce-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="8dfce-114">Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione Seek per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8dfce-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="8dfce-115">Quando l'operazione di scrub è completa, la sessione multimediale Invia un evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfce-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="8dfce-116">Attendere questo evento prima di chiamare di nuovo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per un'altra operazione di pulitura.</span><span class="sxs-lookup"><span data-stu-id="8dfce-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="8dfce-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="8dfce-117">Example</span></span>

<span data-ttu-id="8dfce-118">Nell'esempio di codice riportato di seguito viene illustrato come eseguire lo scrubbing.</span><span class="sxs-lookup"><span data-stu-id="8dfce-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="8dfce-119">Un'operazione di pulitura completata genera l'evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) dopo che tutti i sink di flusso vengono aggiornati con il nuovo frame e l'operazione di pulitura viene completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8dfce-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="8dfce-120">Quando si pulisce un file video, viene visualizzato il frame cercato, ma non viene generato un output audio.</span><span class="sxs-lookup"><span data-stu-id="8dfce-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="8dfce-121">L'applicazione può eseguire lo stepping del frame impostando la velocità di riproduzione su zero e quindi passando un **PROPVARIANT** impostato su **VT \_ empty** nella chiamata a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="8dfce-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dfce-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8dfce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dfce-123">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="8dfce-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="8dfce-124">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="8dfce-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



