---
description: Il formato SAMI (Synchronized Accessible Media Interchange) è un formato per l'aggiunta di didascalie ai supporti digitali.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Origine supporto SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058450"
---
# <a name="sami-media-source"></a><span data-ttu-id="7276d-103">Origine supporto SAMI</span><span class="sxs-lookup"><span data-stu-id="7276d-103">SAMI Media Source</span></span>

<span data-ttu-id="7276d-104">Il formato SAMI (Synchronized Accessible Media Interchange) è un formato per l'aggiunta di didascalie ai supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="7276d-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="7276d-105">Le didascalie vengono archiviate in un file di testo separato con estensione SMI o Sami.</span><span class="sxs-lookup"><span data-stu-id="7276d-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="7276d-106">In Media Foundation i file di didascalia SAMI sono supportati tramite l'origine dei supporti SAMI.</span><span class="sxs-lookup"><span data-stu-id="7276d-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="7276d-107">Usare il [resolver di origine](source-resolver.md) per creare un'istanza dell'origine supporto Sami da un URL o un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="7276d-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="7276d-108">Media Foundation non fornisce un componente che visualizza le didascalie SAMI.</span><span class="sxs-lookup"><span data-stu-id="7276d-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="7276d-109">L'applicazione deve interpretare i dati della didascalia ricevuti dall'origine dei supporti SAMI.</span><span class="sxs-lookup"><span data-stu-id="7276d-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="7276d-110">Di seguito viene illustrato un esempio di file SAMI.</span><span class="sxs-lookup"><span data-stu-id="7276d-110">The following shows an example SAMI file.</span></span>

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

<span data-ttu-id="7276d-111">L' `<STYLE>` elemento contiene informazioni sullo stile.</span><span class="sxs-lookup"><span data-stu-id="7276d-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="7276d-112">Questo esempio contiene uno stile di base per `<P>` gli elementi, insieme a due stili denominati, "standard" e "Hilite".</span><span class="sxs-lookup"><span data-stu-id="7276d-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="7276d-113">Gli stili denominati vengono utilizzati per modificare lo stile di base.</span><span class="sxs-lookup"><span data-stu-id="7276d-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="7276d-114">Le didascalie vengono posizionate all'interno di `<SYNC>` elementi.</span><span class="sxs-lookup"><span data-stu-id="7276d-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="7276d-115">L'attributo Start restituisce il tempo di presentazione in millisecondi per la didascalia.</span><span class="sxs-lookup"><span data-stu-id="7276d-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="7276d-116">Le didascalie di questo esempio sono fornite in due lingue, specificate dai tag di lingua RFC-1766, "en-US" e "fr-FR".</span><span class="sxs-lookup"><span data-stu-id="7276d-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="7276d-117">All'interno delle didascalie, le lingue sono identificate dai rispettivi nomi di classe; in questo caso, "ENUSCC" e "FRFRCC".</span><span class="sxs-lookup"><span data-stu-id="7276d-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="7276d-118">L'origine dei supporti SAMI crea un flusso multimediale per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="7276d-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="7276d-119">Per impostazione predefinita, il primo flusso è selezionato e i flussi rimanenti vengono deselezionati.</span><span class="sxs-lookup"><span data-stu-id="7276d-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="7276d-120">L'applicazione può modificare la selezione del flusso chiamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="7276d-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="7276d-121">Ogni descrittore di flusso contiene gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7276d-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="7276d-122">Attributo</span><span class="sxs-lookup"><span data-stu-id="7276d-122">Attribute</span></span>                                                       | <span data-ttu-id="7276d-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7276d-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="7276d-124">**\_lingua MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="7276d-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="7276d-125">Tag di lingua, come specificato dall' `lang` attributo.</span><span class="sxs-lookup"><span data-stu-id="7276d-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="7276d-126">**\_lingua MF SD \_ Sami \_**</span><span class="sxs-lookup"><span data-stu-id="7276d-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="7276d-127">Nome del linguaggio, come specificato dall' `Name` attributo.</span><span class="sxs-lookup"><span data-stu-id="7276d-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="7276d-128">Ogni flusso ha il seguente tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="7276d-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="7276d-129">Attributo</span><span class="sxs-lookup"><span data-stu-id="7276d-129">Attribute</span></span>                                                                            | <span data-ttu-id="7276d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7276d-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="7276d-131">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="7276d-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="7276d-132">**\_Sami MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7276d-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="7276d-133">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="7276d-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="7276d-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="7276d-134">**TRUE**</span></span>              |



 

<span data-ttu-id="7276d-135">L'origine SAMI recapita ogni didascalia in un esempio di supporto separato.</span><span class="sxs-lookup"><span data-stu-id="7276d-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="7276d-136">Il timestamp e la durata del campione sono derivati dall' `<SYNC>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7276d-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="7276d-137">Il buffer multimediale contenuto nell'esempio contiene la didascalia come testo ASCII.</span><span class="sxs-lookup"><span data-stu-id="7276d-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="7276d-138">Lo stile della didascalia viene incorporato nella didascalia come attributo inline `STYLE` .</span><span class="sxs-lookup"><span data-stu-id="7276d-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="7276d-139">Ad esempio, dato il file SAMI precedente e usando il flusso della lingua inglese con gli stili predefiniti, il primo buffer multimediale conterrebbe i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="7276d-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="7276d-140">(Le interruzioni di riga potrebbero essere diverse da quelle illustrate qui).</span><span class="sxs-lookup"><span data-stu-id="7276d-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="7276d-141">Stili SAMI</span><span class="sxs-lookup"><span data-stu-id="7276d-141">SAMI Styles</span></span>

<span data-ttu-id="7276d-142">Per modificare lo stile corrente, utilizzare l'interfaccia [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="7276d-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="7276d-143">Questa interfaccia viene ottenuta chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sull'origine dei supporti Sami.</span><span class="sxs-lookup"><span data-stu-id="7276d-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="7276d-144">Se si usa l'origine del supporto SAMI con la sessione multimediale, chiamare **GetService** nella sessione multimediale. L'identificatore del servizio è il **\_ \_ servizio MF Sami**.</span><span class="sxs-lookup"><span data-stu-id="7276d-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="7276d-145">Nell'esempio seguente viene impostato lo stile SAMI corrente, specificato da index.</span><span class="sxs-lookup"><span data-stu-id="7276d-145">The following example sets the current SAMI style, specified by index.</span></span>


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



<span data-ttu-id="7276d-146">Questo esempio chiama i metodi seguenti nell'origine supporto SAMI:</span><span class="sxs-lookup"><span data-stu-id="7276d-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="7276d-147">[**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) ottiene il numero di stili.</span><span class="sxs-lookup"><span data-stu-id="7276d-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="7276d-148">[**IMFSAMIStyle:: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) ottiene un elenco dei nomi di stile, archiviati in un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="7276d-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="7276d-149">[**IMFSAMIStyle:: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) imposta uno stile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="7276d-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="7276d-150">L'elenco dei nomi di stile viene archiviato anche nel descrittore della presentazione, nell'attributo di stile dell'elenco di [**\_ \_ \_ stili MF PD Sami**](mf-pd-sami-stylelist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7276d-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7276d-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7276d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7276d-152">Origini e sink multimediali</span><span class="sxs-lookup"><span data-stu-id="7276d-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="7276d-153">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7276d-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



