---
description: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908899"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="5a29b-103">Trasformazioni di pre-elaborazione del decodificatore MPEG</span><span class="sxs-lookup"><span data-stu-id="5a29b-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="5a29b-104">**Letterbox e PanScan**</span><span class="sxs-lookup"><span data-stu-id="5a29b-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="5a29b-105">L'immagine 4x3 può essere formata mediante il riempimento della parte superiore e inferiore dell'immagine (detta immagine Letterbox) o estraendo una parte 4x3 dell'immagine (detta immagine PanScan).</span><span class="sxs-lookup"><span data-stu-id="5a29b-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="5a29b-106">I menu e i flussi delle immagini secondarie sono sovrapposti all'immagine video finale.</span><span class="sxs-lookup"><span data-stu-id="5a29b-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="5a29b-107">Le immagini con rapporto 16x9 vengono archiviate in un formato anamorfico 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="5a29b-108">L'estensione del video di origine anamorfico 4x3 con proporzioni 720x480 a proporzioni 16x9 costituisce l'immagine originale dell'aspetto 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="5a29b-109">Di seguito è riportata una descrizione di come visualizzare correttamente ogni modalità e le relative evidenziazioni:</span><span class="sxs-lookup"><span data-stu-id="5a29b-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="5a29b-110">**Widescreen:** Il video di origine si estende nell'area più grande di 16x9 della finestra di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="5a29b-111">Le evidenziazioni sono relative all'interno dell'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="5a29b-112">Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="5a29b-113">**Analisi panoramica:** Dal video 16x9 usare l'offset orizzontale fornito nel flusso MPEG2 per estrarre una finestra secondaria 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="5a29b-114">Posizionare la finestra secondaria 4x3 nell'area 4x3 più grande della finestra del client di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="5a29b-115">Le coordinate dell'evidenziazione sono relative alla finestra di output 4x3 e non hanno alcuna relazione con il video 16x9 di origine.</span><span class="sxs-lookup"><span data-stu-id="5a29b-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="5a29b-116">Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="5a29b-117">**Letterbox:** Calcolare l'area 4x3 più grande della finestra di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="5a29b-118">Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="5a29b-119">Il video anamorfico 4x3 di origine (che rappresenta un'immagine 16x9) viene posizionato nella finestra secondaria 16x9 più grande all'interno dell'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="5a29b-120">Le barre nere devono essere aggiunte nella parte superiore e inferiore della finestra secondaria per mantenere un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="5a29b-121">Le coordinate dell'evidenziazione sono relative all'area 4x3 e non hanno alcuna relazione con il video 16x9 di origine.</span><span class="sxs-lookup"><span data-stu-id="5a29b-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="5a29b-122">È possibile per un disco specificare un'evidenziazione che si trova all'esterno dell'area 16x9 (ma ancora nella finestra 4x3).</span><span class="sxs-lookup"><span data-stu-id="5a29b-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="5a29b-123">Per il video 4x3, il video viene inserito nell'area di output 4x3 più grande della finestra del client di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="5a29b-124">Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="5a29b-125">**Pre-elaborazione MPEG con lo strumento di spostamento DVD e VMR**</span><span class="sxs-lookup"><span data-stu-id="5a29b-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="5a29b-126">Attualmente al decodificatore viene passato un tipo di supporto FORMAT MPEG2 VIDEO (il cui blocco di formato punta \_ \_ a una struttura [**MPEG2VIDEOINFO).**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)</span><span class="sxs-lookup"><span data-stu-id="5a29b-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="5a29b-127">Sui pin di output, il decodificatore produce un tipo di supporto FORMAT VideoInfo2, il cui blocco di formato punta \_ a una [**struttura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="5a29b-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="5a29b-128">Il campo **dwReserved** della struttura è stato rinominato in **flag dwControls.**</span><span class="sxs-lookup"><span data-stu-id="5a29b-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="5a29b-129">Il **membro dwControlFlags** conterrà ora i nuovi bit.</span><span class="sxs-lookup"><span data-stu-id="5a29b-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="5a29b-130">Label</span><span class="sxs-lookup"><span data-stu-id="5a29b-130">Label</span></span> | <span data-ttu-id="5a29b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5a29b-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="5a29b-132">AMCONTROL \_ USATO</span><span class="sxs-lookup"><span data-stu-id="5a29b-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="5a29b-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5a29b-133">0x00000001</span></span> |
| <span data-ttu-id="5a29b-134">AMCONTROL \_ PAD \_ TO \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="5a29b-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="5a29b-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5a29b-135">0x00000002</span></span> |
| <span data-ttu-id="5a29b-136">AMCONTROL \_ PAD \_ TO \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="5a29b-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="5a29b-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5a29b-137">0x00000004</span></span> |



 

<span data-ttu-id="5a29b-138">AMCONTROL \_ USED viene usato per verificare se questi nuovi flag sono supportati.</span><span class="sxs-lookup"><span data-stu-id="5a29b-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="5a29b-139">Un filtro di origine deve impostare il flag AMCONTROL USED e verificare se \_ QueryAccept(MediaType) ha esito positivo sul pin downstream.</span><span class="sxs-lookup"><span data-stu-id="5a29b-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="5a29b-140">Se viene rifiutato, non è possibile usare i flag AMCONTROL e dwReserved1 deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="5a29b-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="5a29b-141">AMCONTROL PAD TO 4x3 indica che l'immagine deve essere riempita e visualizzata \_ \_ in \_ un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="5a29b-142">AMCONTROL PAD TO 16x9 indica che l'immagine deve essere riempita e visualizzata \_ \_ in \_ un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="5a29b-143">Il decodificatore deve copiare o elaborare i bit in modo blindato.</span><span class="sxs-lookup"><span data-stu-id="5a29b-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="5a29b-144">Se il decodificatore esegue il letterboxing, deve modificare le proporzioni dei pixel, riempire l'immagine e rimuovere i bit AMCONTROL \_ \* corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="5a29b-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="5a29b-145">MPEG2VIDEOINFO.dwFlags contiene ora tre flag per controllare la modalità di visualizzazione del contenuto:</span><span class="sxs-lookup"><span data-stu-id="5a29b-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="5a29b-146">`AMMPEG2_DoPanScan (0x00000001)`: se questo flag è impostato, il decodificatore video MPEG-2 deve ritagliare l'immagine di output in base ai vettori di scansione panoramica nell'estensione di visualizzazione dell'immagine e modificare le proporzioni dell'immagine in \_ \_ 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="5a29b-147">Il vmr non deve ricevere un esempio 16x9 con questo flag.</span><span class="sxs-lookup"><span data-stu-id="5a29b-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="5a29b-148">Un'implementazione semplice potrebbe modificare il rettangolo di origine per indicare un'area di origine di 540 larghezza con un bordo sinistro uguale all'offset di visualizzazione nell'estensione di \_ visualizzazione \_ dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5a29b-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="5a29b-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: quando un decodificatore hardware visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve applicare le regole per la visualizzazione di un campione 16x9 su un display 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="5a29b-150">Un decodificatore software (o un decodificatore hardware che produce l'output inviato al VMR) ha due opzioni per l'elaborazione delle immagini:</span><span class="sxs-lookup"><span data-stu-id="5a29b-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="5a29b-151">Ignorare questo flag e passare il contenuto di VideoInfoHeader2 al VMR(il flag AMCONTROL PAD TO 4x3 sarà già impostato dallo strumento di navigazione \_ \_ \_ [DVD](dvd-navigator-filter.md) nell'esempio).</span><span class="sxs-lookup"><span data-stu-id="5a29b-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="5a29b-152">La macchina virtuale risconterà un esempio di video 16x9 con il flag AMCONTROL PAD TO 4x3 impostato e un flusso di immagini secondarie \_ \_ \_ 4x3.</span><span class="sxs-lookup"><span data-stu-id="5a29b-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="5a29b-153">L'applicazione deve impostare i rettangoli di destinazione normalizzati di output dei due flussi sulla stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="5a29b-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="5a29b-154">Convertire il flusso anamorfico in un'immagine 4x3 mediante il riempimento della parte superiore e inferiore dell'immagine e l'impostazione delle proporzioni dell'immagine su 4x3 (vedere Letterbox sopra) e rimuovendo AMCONTROL \_ PAD \_ a \_ 4x3 bit da VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="5a29b-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="5a29b-155">I decodificatori DirectXVA che combinano i flussi video e di immagini secondarie devono elaborare questo flag.</span><span class="sxs-lookup"><span data-stu-id="5a29b-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="5a29b-156">Se l'hardware non è in grado di ridimensionare l'immagine secondaria blended, il decodificatore deve produrre un flusso di immagini secondarie separato per la vmr per la fusione con il video.</span><span class="sxs-lookup"><span data-stu-id="5a29b-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="5a29b-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: quando un decodificatore hardware visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve presupporre un display 16x9 (anamorfico).</span><span class="sxs-lookup"><span data-stu-id="5a29b-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="5a29b-158">Un decodificatore software (o un decodificatore hardware che produce l'output inviato al VMR) ha due opzioni per l'elaborazione di un'immagine anamorfica:</span><span class="sxs-lookup"><span data-stu-id="5a29b-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="5a29b-159">Ignorare questo flag e copiare il contenuto di VideoInfoHeader2 nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a29b-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="5a29b-160">La macchina virtuale inserirà immagini da 4 x 3 a 16x9 se è impostata l'opzione AMCONTROL \_ PAD \_ TO \_ 16x9.</span><span class="sxs-lookup"><span data-stu-id="5a29b-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="5a29b-161">Riempire l'immagine di output in un'immagine 16x9 e rimuovere IL PAD AMCONTROL \_ \_ a \_ 16x9 bit.</span><span class="sxs-lookup"><span data-stu-id="5a29b-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="5a29b-162">La maggior parte dei decodificatori deve usare **GetMediaType** per rilevare una modifica del supporto sul pin di input e copiare il contenuto **VIDEOINFOHEADER2** (contenuto in **MPEG2INFOHEADER)** nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="5a29b-163">Probabilmente elaelaborare solo il bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="5a29b-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="5a29b-164">Il codice di esempio seguente illustra come copiare il **contenuto VIDEOINFOHEADER2** da un pin di input a un pin di output.</span><span class="sxs-lookup"><span data-stu-id="5a29b-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



