---
description: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747055"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="0e8b8-103">Trasformazioni di pre-elaborazione del decodificatore MPEG</span><span class="sxs-lookup"><span data-stu-id="0e8b8-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="0e8b8-104">**Letterbox e PanScan**</span><span class="sxs-lookup"><span data-stu-id="0e8b8-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="0e8b8-105">L'immagine 4x3 può essere costituita dall'imbottitura della parte superiore e inferiore dell'immagine (detta immagine letterbox) o dall'estrazione di una parte 4x3 dell'immagine (denominata immagine PanScan).</span><span class="sxs-lookup"><span data-stu-id="0e8b8-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="0e8b8-106">I menu e i flussi di sottoimmagine sono sovrapposti sopra l'immagine video finale.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="0e8b8-107">Le immagini del rapporto 16x9 vengono archiviate in un formato 4x3 Anamorfo.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="0e8b8-108">L'allungamento del video di origine 720x480 4x3 proporzionale a una proporzione 16x9 rappresenta l'immagine dell'aspetto 16x9 originale.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="0e8b8-109">Di seguito è riportata una descrizione del modo in cui vengono visualizzate correttamente le modalità e le relative caratteristiche principali:</span><span class="sxs-lookup"><span data-stu-id="0e8b8-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="0e8b8-110">**Widescreen:** Il video di origine esteso nell'area 16x9 più grande della finestra di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="0e8b8-111">Le evidenziazioni sono relative all'interno dell'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="0e8b8-112">Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="0e8b8-113">**Panoramica dell'analisi:** Dal video 16x9, usare l'offset orizzontale specificato nel flusso MPEG2 per estrarre una sottofinestra 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="0e8b8-114">Posizionare la sottofinestra 4x3 nell'area 4x3 più grande della finestra client di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="0e8b8-115">Le coordinate dell'evidenziazione sono relative alla finestra di output di 4x3 e non hanno alcuna relazione con il video 16x9 di origine.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="0e8b8-116">Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="0e8b8-117">**Letterbox:** Calcola l'area 4x3 più grande della finestra di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="0e8b8-118">Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="0e8b8-119">Il video 4x3 Anamorfo di origine (che rappresenta un'immagine 16x9) viene inserito nella sottofinestra 16x9 più grande all'interno dell'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="0e8b8-120">Le barre nere devono essere aggiunte alla parte superiore e inferiore della sottofinestra per mantenere un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="0e8b8-121">Le coordinate dell'evidenziazione sono relative all'area 4x3 e non hanno alcuna relazione con il video 16x9 di origine.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="0e8b8-122">È possibile che un disco specifichi un'evidenziazione che si trova al di fuori dell'area di 16x9 (ma ancora nella finestra 4x3).</span><span class="sxs-lookup"><span data-stu-id="0e8b8-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="0e8b8-123">Per 4x3 video, il video viene inserito nell'area di output 4x3 più grande della finestra client di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="0e8b8-124">Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="0e8b8-125">**Pre-elaborazione MPEG con DVD Navigator e VMR**</span><span class="sxs-lookup"><span data-stu-id="0e8b8-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="0e8b8-126">Al momento, al decodificatore viene passato un \_ \_ tipo di supporto video MPEG2 di formato (il cui blocco di formato punta a una struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ).</span><span class="sxs-lookup"><span data-stu-id="0e8b8-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="0e8b8-127">Nei pin di output, il decodificatore produce un formato \_ VideoInfo2 tipo di supporto, il cui blocco di formato punta a una struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="0e8b8-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="0e8b8-128">Il campo **dwReserved** della struttura è stato rinominato in flag **dwControls** .</span><span class="sxs-lookup"><span data-stu-id="0e8b8-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="0e8b8-129">Il membro **dwControlFlags** conterrà ora i nuovi bit.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-129">The **dwControlFlags** member will now contain the new bits.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="0e8b8-130">AMCONTROL \_ usato</span><span class="sxs-lookup"><span data-stu-id="0e8b8-130">AMCONTROL\_USED</span></span>          | <span data-ttu-id="0e8b8-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0e8b8-131">0x00000001</span></span> |
| <span data-ttu-id="0e8b8-132">AMCONTROL \_ Pad \_ \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="0e8b8-132">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="0e8b8-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0e8b8-133">0x00000002</span></span> |
| <span data-ttu-id="0e8b8-134">AMCONTROL \_ Pad \_ \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="0e8b8-134">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="0e8b8-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0e8b8-135">0x00000004</span></span> |



 

<span data-ttu-id="0e8b8-136">AMCONTROL \_ usato per verificare se questi nuovi flag sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-136">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="0e8b8-137">Un filtro di origine deve impostare il \_ flag usato AMCONTROL e verificare se QueryAccept (mediaType) ha esito positivo sul pin downstream.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-137">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="0e8b8-138">Se viene rifiutato, non è possibile usare i flag AMCONTROL e dwReserved1 deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-138">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="0e8b8-139">AMCONTROL \_ Pad \_ \_ 4x3 indica che l'immagine deve essere riempita e visualizzata in un'area 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-139">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="0e8b8-140">AMCONTROL \_ Pad \_ \_ 16x9 indica che l'immagine deve essere riempita e visualizzata in un'area 16x9.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-140">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="0e8b8-141">Il decodificatore deve copiare o elaborare in modo cieco i bit.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-141">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="0e8b8-142">Se il decodificatore esegue il letterboxing, deve modificare le proporzioni dei pixel, riempire l'immagine e rimuovere i bit AMCONTROL corrispondenti \_ \* .</span><span class="sxs-lookup"><span data-stu-id="0e8b8-142">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="0e8b8-143">MPEG2VIDEOINFO. dwFlags contiene ora tre flag per il controllo della modalità di visualizzazione del contenuto:</span><span class="sxs-lookup"><span data-stu-id="0e8b8-143">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="0e8b8-144">`AMMPEG2_DoPanScan (0x00000001)`: Se questo flag è impostato, il decodificatore MPEG-2 video dovrebbe ritagliare l'immagine di output in base ai vettori di analisi panoramica nell' \_ \_ estensione per la visualizzazione dell'immagine e modificare le proporzioni dell'immagine in 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-144">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="0e8b8-145">VMR non deve ricevere un esempio 16x9 con questo flag.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-145">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="0e8b8-146">Un'implementazione semplice potrebbe modificare il rettangolo di origine per indicare un'area di origine di 540 Wide con un bordo sinistro uguale all'offset di visualizzazione nell'estensione per la visualizzazione dell'immagine \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e8b8-146">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="0e8b8-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Quando un decodificatore hardware Visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve applicare le regole per la visualizzazione di un esempio 16x9 in una visualizzazione 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="0e8b8-148">Un decodificatore software (o un decodificatore hardware che produce output inviato a VMR) dispone di due opzioni per l'elaborazione delle immagini:</span><span class="sxs-lookup"><span data-stu-id="0e8b8-148">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="0e8b8-149">Ignorare questo flag e passare il contenuto di VideoInfoHeader2 a VMR (il \_ flag AMCONTROL \_ \_ su 4x3 sarà già impostato dal [navigatore DVD](dvd-navigator-filter.md) nell'esempio).</span><span class="sxs-lookup"><span data-stu-id="0e8b8-149">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="0e8b8-150">VMR incontrerà un esempio video 16x9 con AMCONTROL \_ Pad \_ per \_ 4x3 flag impostati e un flusso di sottoimmagine 4x3.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-150">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="0e8b8-151">L'applicazione deve impostare i rettangoli di destinazione normalizzati di output dei due flussi in modo che abbiano la stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-151">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="0e8b8-152">Convertire il flusso Anamorfo in un'immagine 4x3, affiancando la parte superiore e inferiore dell'immagine e impostando le proporzioni dell'immagine su 4x3 (vedere la cassetta post precedente) e rimuovendo il \_ riquadro AMCONTROL \_ in \_ 4x3 bit da VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-152">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="0e8b8-153">I decodificatori DirectXVA che combinano i flussi video e subpicture dovranno elaborare questo flag.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-153">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="0e8b8-154">Se l'hardware non è in grado di ridimensionare la sottoimmagine sfumata, il decodificatore deve produrre un flusso di sottoimmagine separato affinché VMR si mescoli con il video.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-154">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="0e8b8-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Quando un decodificatore hardware Visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve presupporre una visualizzazione 16x9 (Anamorfo).</span><span class="sxs-lookup"><span data-stu-id="0e8b8-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="0e8b8-156">Un decodificatore software (o un decodificatore hardware che produce output inviato a VMR) dispone di due opzioni per l'elaborazione di un'immagine anamorfica:</span><span class="sxs-lookup"><span data-stu-id="0e8b8-156">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="0e8b8-157">Ignorare questo flag e copiare il contenuto di VideoInfoHeader2 in VMR.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-157">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="0e8b8-158">VMR comporterà il riempimento delle immagini 4x3 in 16x9 se il \_ riquadro AMCONTROL è \_ \_ impostato su 16x9.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-158">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="0e8b8-159">Aggiungere l'immagine di output a un'immagine 16x9 e rimuovere AMCONTROL \_ Pad \_ \_ 16x9 bit.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-159">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="0e8b8-160">La maggior parte dei decodificatori deve usare **GetMediaType** per rilevare una modifica del supporto del PIN di input e copiare il contenuto di **VIDEOINFOHEADER2** (contenuto nel **MPEG2INFOHEADER**) nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-160">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="0e8b8-161">Probabilmente verranno elaborati solo il bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-161">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="0e8b8-162">Il codice di esempio seguente mostra come copiare il contenuto di **VIDEOINFOHEADER2** da un pin di input in un pin di output.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-162">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


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



 

 



