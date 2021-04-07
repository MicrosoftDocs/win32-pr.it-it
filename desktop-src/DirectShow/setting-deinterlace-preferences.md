---
description: Impostazione delle preferenze di deinterlacciamento
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Impostazione delle preferenze di deinterlacciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745407"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="25aab-103">Impostazione delle preferenze di deinterlacciamento</span><span class="sxs-lookup"><span data-stu-id="25aab-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="25aab-104">Il renderer video mixing (VMR) supporta il deinterlacciamento con accelerazione hardware, che migliora la qualità del rendering per i video interlacciati.</span><span class="sxs-lookup"><span data-stu-id="25aab-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="25aab-105">Le funzionalità esatte disponibili dipendono dall'hardware sottostante.</span><span class="sxs-lookup"><span data-stu-id="25aab-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="25aab-106">L'applicazione può eseguire una query per le funzionalità di deinterlacciamento hardware e impostare le preferenze di deinterlacciamento tramite l'interfaccia [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) o [**IVMRDEINTERLACECONTROL9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) Interface (VMR-9).</span><span class="sxs-lookup"><span data-stu-id="25aab-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="25aab-107">Il deinterlacciamento viene eseguito in base al flusso.</span><span class="sxs-lookup"><span data-stu-id="25aab-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="25aab-108">Esiste una differenza importante nel comportamento di interlacciamento tra VMR-7 e VMR-9.</span><span class="sxs-lookup"><span data-stu-id="25aab-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="25aab-109">Nei sistemi in cui l'hardware grafico non supporta la deinterlacciamento avanzata, VMR-7 può eseguire il fallback alla sovrapposizione hardware e indicare all'utente di usare uno stile di deinterlacciamento BOB.</span><span class="sxs-lookup"><span data-stu-id="25aab-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="25aab-110">In questo caso, anche se VMR segnala 30 fps, il video viene effettivamente sottoposto a rendering a 60 flip al secondo.</span><span class="sxs-lookup"><span data-stu-id="25aab-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="25aab-111">Tranne nel caso di VMR-7 utilizzando la sovrimpressione hardware, il deinterlacciamento viene eseguito dal mixer di VMR.</span><span class="sxs-lookup"><span data-stu-id="25aab-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="25aab-112">Per eseguire il deinterlacciamento, il mixer usa l'interfaccia DDI per l'accelerazione video DirectX (DXVA) deinterlacciamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25aab-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="25aab-113">Questo DDI non è richiamabile dalle applicazioni e le applicazioni non possono sostituire la funzionalità di deinterlacciamento di VMR.</span><span class="sxs-lookup"><span data-stu-id="25aab-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="25aab-114">Tuttavia, un'applicazione può selezionare la modalità di deinterlacciamento desiderata, come descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="25aab-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="25aab-115">In questa sezione vengono descritti i metodi **IVMRDeinterlaceControl9** , ma le versioni VMR-7 sono quasi identiche.</span><span class="sxs-lookup"><span data-stu-id="25aab-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="25aab-116">Per ottenere le funzionalità di deinterlacciamento per un flusso video, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25aab-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="25aab-117">Compilare una struttura [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) con una descrizione del flusso video.</span><span class="sxs-lookup"><span data-stu-id="25aab-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="25aab-118">I dettagli su come compilare questa struttura sono forniti in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="25aab-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="25aab-119">Passare la struttura al metodo [**IVMRDeinterlaceControl9:: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) .</span><span class="sxs-lookup"><span data-stu-id="25aab-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="25aab-120">Chiamare il metodo due volte.</span><span class="sxs-lookup"><span data-stu-id="25aab-120">Call the method twice.</span></span> <span data-ttu-id="25aab-121">La prima chiamata restituisce il numero di modalità di deinterlacciamento supportate dall'hardware per il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="25aab-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="25aab-122">Allocare una matrice di GUID di queste dimensioni e chiamare di nuovo il metodo, passando l'indirizzo della matrice.</span><span class="sxs-lookup"><span data-stu-id="25aab-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="25aab-123">La seconda chiamata compila la matrice con i GUID.</span><span class="sxs-lookup"><span data-stu-id="25aab-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="25aab-124">Ogni GUID identifica una modalità di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="25aab-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="25aab-125">Per ottenere il capabiltiies di una particolare modalità, chiamare il metodo [**IVMRDeinterlaceControl9:: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) .</span><span class="sxs-lookup"><span data-stu-id="25aab-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="25aab-126">Passare la stessa struttura **VMR9VideoDesc** , insieme a uno dei GUID della matrice.</span><span class="sxs-lookup"><span data-stu-id="25aab-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="25aab-127">Il metodo compila una struttura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) con le funzionalità della modalità.</span><span class="sxs-lookup"><span data-stu-id="25aab-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="25aab-128">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="25aab-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="25aab-129">A questo punto, l'applicazione può impostare la modalità di deinterlacciamento per il flusso, usando i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="25aab-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="25aab-130">Il metodo [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) imposta la modalità preferita.</span><span class="sxs-lookup"><span data-stu-id="25aab-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="25aab-131">Utilizzare il GUID \_ null per disattivare il deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="25aab-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="25aab-132">Il metodo [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) specifica il comportamento se la modalità richiesta non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="25aab-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="25aab-133">Il metodo [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) restituisce la modalità preferita impostata.</span><span class="sxs-lookup"><span data-stu-id="25aab-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="25aab-134">Il metodo [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) restituisce la modalità effettiva in uso, che potrebbe essere una modalità di fallback, se la modalità preferita non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="25aab-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="25aab-135">Le pagine di riferimento del metodo forniscono ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="25aab-135">The method reference pages give more information.</span></span>

<span data-ttu-id="25aab-136">**Uso della struttura VMR9VideoDesc**</span><span class="sxs-lookup"><span data-stu-id="25aab-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="25aab-137">Nella procedura indicata in precedenza, il primo passaggio consiste nel compilare una struttura **VMR9VideoDesc** con una descrizione del flusso video.</span><span class="sxs-lookup"><span data-stu-id="25aab-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="25aab-138">Per iniziare, ottenere il tipo di supporto del flusso video.</span><span class="sxs-lookup"><span data-stu-id="25aab-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="25aab-139">È possibile eseguire questa operazione chiamando [**Ipin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) sul pin di input del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="25aab-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="25aab-140">Verificare quindi se il flusso video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="25aab-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="25aab-141">Solo i formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) possono essere interlacciati.</span><span class="sxs-lookup"><span data-stu-id="25aab-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="25aab-142">Se il formato del tipo è \_ videoinfo, deve essere un frame progressivo.</span><span class="sxs-lookup"><span data-stu-id="25aab-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="25aab-143">Se il formato del tipo è \_ VideoInfo2, selezionare il campo **dwInterlaceFlags** per il \_ flag AMINTERLACE interlacciato.</span><span class="sxs-lookup"><span data-stu-id="25aab-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="25aab-144">La presenza di questo flag indica che il video è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="25aab-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="25aab-145">Si supponga che la variabile **pBMI** sia un puntatore alla struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="25aab-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="25aab-146">Impostare i valori seguenti nella struttura **VMR9VideoDesc** :</span><span class="sxs-lookup"><span data-stu-id="25aab-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="25aab-147">**dwSize**: impostare questo campo su `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="25aab-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="25aab-148">**dwSampleWidth**: impostare questo campo su `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="25aab-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="25aab-149">**dwSampleHeight**: impostare questo campo su `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="25aab-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="25aab-150">**SampleFormat**: questo campo descrive le caratteristiche di interlacciamento del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="25aab-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="25aab-151">Controllare il campo **dwInterlaceFlags** nella struttura **VIDEOINFOHEADER2** e impostare **SampleFormat** uguale al flag [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente.</span><span class="sxs-lookup"><span data-stu-id="25aab-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="25aab-152">Di seguito è riportata una funzione helper a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="25aab-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="25aab-153">**InputSampleFreq**: questo campo fornisce la frequenza di input, che può essere calcolata dal campo **AvgTimePerFrame** nella struttura **VIDEOINFOHEADER2** .</span><span class="sxs-lookup"><span data-stu-id="25aab-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="25aab-154">Nel caso generale, impostare **dwNumerator** su 10 milioni e impostare **dwDenominator** su **AvgTimePerFrame**.</span><span class="sxs-lookup"><span data-stu-id="25aab-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="25aab-155">Tuttavia, è anche possibile verificare la presenza di alcune frequenze dei fotogrammi note:</span><span class="sxs-lookup"><span data-stu-id="25aab-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="25aab-156">Tempo medio per fotogramma</span><span class="sxs-lookup"><span data-stu-id="25aab-156">Average time per frame</span></span> | <span data-ttu-id="25aab-157">Frequenza fotogrammi (fps)</span><span class="sxs-lookup"><span data-stu-id="25aab-157">Frame rate (fps)</span></span> | <span data-ttu-id="25aab-158">Numeratore</span><span class="sxs-lookup"><span data-stu-id="25aab-158">Numerator</span></span> | <span data-ttu-id="25aab-159">Denominatore</span><span class="sxs-lookup"><span data-stu-id="25aab-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="25aab-160">166833</span><span class="sxs-lookup"><span data-stu-id="25aab-160">166833</span></span>                 | <span data-ttu-id="25aab-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="25aab-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="25aab-162">60000</span><span class="sxs-lookup"><span data-stu-id="25aab-162">60000</span></span>     | <span data-ttu-id="25aab-163">1001</span><span class="sxs-lookup"><span data-stu-id="25aab-163">1001</span></span>        |
    | <span data-ttu-id="25aab-164">333667</span><span class="sxs-lookup"><span data-stu-id="25aab-164">333667</span></span>                 | <span data-ttu-id="25aab-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="25aab-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="25aab-166">30000</span><span class="sxs-lookup"><span data-stu-id="25aab-166">30000</span></span>     | <span data-ttu-id="25aab-167">1001</span><span class="sxs-lookup"><span data-stu-id="25aab-167">1001</span></span>        |
    | <span data-ttu-id="25aab-168">417188</span><span class="sxs-lookup"><span data-stu-id="25aab-168">417188</span></span>                 | <span data-ttu-id="25aab-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="25aab-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="25aab-170">24000</span><span class="sxs-lookup"><span data-stu-id="25aab-170">24000</span></span>     | <span data-ttu-id="25aab-171">1001</span><span class="sxs-lookup"><span data-stu-id="25aab-171">1001</span></span>        |
    | <span data-ttu-id="25aab-172">200000</span><span class="sxs-lookup"><span data-stu-id="25aab-172">200000</span></span>                 | <span data-ttu-id="25aab-173">50,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="25aab-173">50.00 (PAL)</span></span>      | <span data-ttu-id="25aab-174">50</span><span class="sxs-lookup"><span data-stu-id="25aab-174">50</span></span>        | <span data-ttu-id="25aab-175">1</span><span class="sxs-lookup"><span data-stu-id="25aab-175">1</span></span>           |
    | <span data-ttu-id="25aab-176">400000</span><span class="sxs-lookup"><span data-stu-id="25aab-176">400000</span></span>                 | <span data-ttu-id="25aab-177">25,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="25aab-177">25.00 (PAL)</span></span>      | <span data-ttu-id="25aab-178">25</span><span class="sxs-lookup"><span data-stu-id="25aab-178">25</span></span>        | <span data-ttu-id="25aab-179">1</span><span class="sxs-lookup"><span data-stu-id="25aab-179">1</span></span>           |
    | <span data-ttu-id="25aab-180">416667</span><span class="sxs-lookup"><span data-stu-id="25aab-180">416667</span></span>                 | <span data-ttu-id="25aab-181">24,00 (film)</span><span class="sxs-lookup"><span data-stu-id="25aab-181">24.00 (Film)</span></span>     | <span data-ttu-id="25aab-182">24</span><span class="sxs-lookup"><span data-stu-id="25aab-182">24</span></span>        | <span data-ttu-id="25aab-183">1</span><span class="sxs-lookup"><span data-stu-id="25aab-183">1</span></span>           |

    

     

-   <span data-ttu-id="25aab-184">**OutputFrameFreq**: questo campo fornisce la frequenza di output, che può essere calcolata dal valore **InputSampleFreq** e dalle caratteristiche di interfoliazione del flusso di input:</span><span class="sxs-lookup"><span data-stu-id="25aab-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="25aab-185">Impostare **OutputFrameFreq. dwDenominator** uguale a **InputSampleFreq. dwDenominator**.</span><span class="sxs-lookup"><span data-stu-id="25aab-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="25aab-186">Se il video di input è Interleaved, impostare **OutputFrameFreq. dwNumerator** su 2 x **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="25aab-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="25aab-187">(Dopo la deinterlacciamento, la frequenza dei fotogrammi è raddoppiata). In caso contrario, impostare il valore su **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="25aab-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="25aab-188">**dwFourCC**: impostare questo campo su `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="25aab-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="25aab-189">La funzione helper seguente converte \_ i flag AMINTERLACE *X* in [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) valori:</span><span class="sxs-lookup"><span data-stu-id="25aab-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



