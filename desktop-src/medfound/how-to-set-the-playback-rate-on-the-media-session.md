---
description: Come impostare la velocità di riproduzione nella sessione multimediale
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Come impostare la velocità di riproduzione nella sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761369"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="eadd0-103">Come impostare la velocità di riproduzione nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="eadd0-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="eadd0-104">Per implementare la funzionalità di riproduzione, ad esempio l'avanzamento rapido e il rewind, è possibile che le applicazioni debbano modificare la velocità di riproduzione per un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="eadd0-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="eadd0-105">Media Foundation fornisce il servizio di controllo della velocità che le applicazioni devono utilizzare per impostare dinamicamente la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eadd0-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="eadd0-106">Prima di impostare la velocità di riproduzione, un'applicazione deve controllare se la frequenza è supportata dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="eadd0-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="eadd0-107">Per informazioni sulle frequenze supportate, vedere [come determinare le tariffe supportate](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="eadd0-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="eadd0-108">Per informazioni sulle frequenze di riproduzione, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="eadd0-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="eadd0-109">Per impostare la velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eadd0-109">To set the playback rate</span></span>

1.  <span data-ttu-id="eadd0-110">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'oggetto di controllo della velocità dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="eadd0-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="eadd0-111">Le applicazioni che chiamano [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devono garantire quanto segue:</span><span class="sxs-lookup"><span data-stu-id="eadd0-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="eadd0-112">Il parametro *punkObject* contiene un puntatore a interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato.</span><span class="sxs-lookup"><span data-stu-id="eadd0-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="eadd0-113">L'oggetto frequenza di controllo ricevuto nel parametro *ppvObject* viene rilasciato per evitare perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="eadd0-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="eadd0-114">Chiamare il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue per impostare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eadd0-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="eadd0-115">Al termine dell'esecuzione della **velocità** in modo asincrono, l'applicazione riceve l'evento [MESessionRateChanged](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="eadd0-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="eadd0-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="eadd0-116">Example</span></span>

<span data-ttu-id="eadd0-117">Il codice seguente illustra come impostare la velocità di riproduzione chiamando il metodo [**serate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .</span><span class="sxs-lookup"><span data-stu-id="eadd0-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



<span data-ttu-id="eadd0-118">L'applicazione deve essere arrestata o sospesa prima di poter eseguire una transizione da una velocità negativa o zero a una velocità positiva.</span><span class="sxs-lookup"><span data-stu-id="eadd0-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="eadd0-119">Per informazioni su questi Stati, vedere [come controllare gli Stati di presentazione](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="eadd0-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eadd0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eadd0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eadd0-121">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="eadd0-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="eadd0-122">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="eadd0-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="eadd0-123">Ricerca, avanzamento rapido e riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="eadd0-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



