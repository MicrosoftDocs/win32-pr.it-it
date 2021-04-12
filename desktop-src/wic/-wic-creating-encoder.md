---
description: Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Panoramica della codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233542"
---
# <a name="encoding-overview"></a>Panoramica della codifica

Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso. L'uso di alcuni codificatori comporta compromessi, ad esempio JPEG, che commercia le informazioni sui colori per una migliore compressione. Gli altri codificatori non generano tali perdite, ad esempio bitmap (BMP). Poiché molti codec usano la tecnologia proprietaria per ottenere una migliore compressione e fedeltà delle immagini, i dettagli sul modo in cui un'immagine viene codificata sono gli sviluppatori di codec.

In questo argomento sono incluse le sezioni seguenti.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Esempio di codifica TIFF](#tiff-encoding-example)
-   [Utilizzo delle opzioni del codificatore](#encoder-options-usage)
-   [Opzioni del codificatore](#encoder-options-usage)
-   [Esempi di opzioni del codificatore](#encoder-options-examples)
-   [Argomenti correlati](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) è l'interfaccia principale per la codifica di un'immagine nel formato di destinazione e usata per serializzare i componenti di un'immagine, ad esempio l'anteprima ([**dithumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e i frame ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), nel file di immagine.

Il modo e il momento in cui viene eseguita la serializzazione viene lasciato allo sviluppatore di codec. Ogni singolo blocco di dati nel formato di file di destinazione deve essere in grado di impostare in modo indipendente dall'ordine, ma anche in questo caso si tratta della decisione dello sviluppatore di codec. Quando viene chiamato il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) , tuttavia, le modifiche all'immagine non devono essere consentite e il flusso deve essere chiuso.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) è l'interfaccia per la codifica dei singoli frame di un'immagine. Fornisce metodi per l'impostazione di singoli componenti per la creazione di immagini di frame, ad esempio anteprime e frame, oltre a formati di dimensioni immagine, DPI e pixel.

I singoli frame possono essere codificati con metadati specifici del frame, in modo che [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) fornisca l'accesso a un writer di metadati tramite il metodo [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

Il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del frame consente di eseguire il commit di tutte le modifiche apportate al singolo frame e indica che le modifiche apportate al frame non devono essere più accettate.

## <a name="tiff-encoding-example"></a>Esempio di codifica TIFF

Nell'esempio seguente viene codificata un'immagine Tagged Image File Format (TIFF) utilizzando [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). L'output TIFF è personalizzato con [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e il frame bitmap viene inizializzato usando le opzioni specificate. Dopo che l'immagine è stata creata con [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), il frame viene sottoposto a commit tramite [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e l'immagine viene salvata tramite [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Utilizzo delle opzioni del codificatore

Codificatori diversi per formati diversi devono esporre opzioni diverse per la modalità di codifica di un'immagine. Windows Imaging Component (WIC) fornisce un meccanismo coerente per esprimere se le opzioni di codifica sono necessarie pur continuando a consentire alle applicazioni di usare più codificatori senza richiedere la conoscenza di un particolare formato. Questa operazione viene eseguita fornendo un parametro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) nel metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e nel metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .

Il componente Factory fornisce un semplice punto di creazione per la creazione di un contenitore delle proprietà Opzioni del codificatore. I codec possono utilizzare questo servizio se è necessario fornire un set semplice, intuitivo e non in conflitto di opzioni del codificatore. Il contenitore delle proprietà di imaging deve essere inizializzato durante la creazione con tutte le opzioni del codificatore rilevanti per il codec. Per le opzioni del codificatore dal set canonico, l'intervallo di valori verrà applicato durante la scrittura. Per esigenze più avanzate, i codec devono scrivere la propria implementazione del contenitore delle proprietà.

Un'applicazione riceve il contenitore delle opzioni del codificatore durante la creazione del frame e deve configurare tutti i valori prima dell'inizializzazione del frame del codificatore. Per un'applicazione basata su interfaccia utente, può offrire un'interfaccia utente fissa per le opzioni del codificatore canonico e una visualizzazione avanzata per le opzioni rimanenti. Le modifiche possono essere apportate una alla volta tramite il metodo Write e tutti gli errori vengono segnalati tramite IErrorLog. L'applicazione dell'interfaccia utente deve sempre rileggere e visualizzare tutte le opzioni dopo avere apportato una modifica nel caso in cui la modifica abbia causato un effetto a cascata. Un'applicazione deve essere preparata per gestire l'inizializzazione non riuscita dei frame per i codec che forniscono solo una segnalazione minima degli errori tramite il contenitore delle proprietà.

## <a name="encoder-options"></a>Opzioni del codificatore

Si può prevedere che un'applicazione riscontri il set di opzioni del codificatore seguente. Le opzioni del codificatore riflettono le funzionalità di un codificatore e il formato del contenitore sottostante e pertanto sono di natura non indipendenti dal codec. Quando possibile, è necessario normalizzare le nuove opzioni in modo che possano essere applicate ai nuovi codec che emergono.



| Nome della proprietà      | VARTYPE  | Valore                                                                     | Codec applicabili |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | \_R4 VT   | 0-1.0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | \_R4 VT   | 0-1.0                                                                     | TIFF              |
| Lossless           | \_bool VT | **true**, **false**                                                       | HDPhoto           |
| BitmapTransform    | \_Ui1 VT  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty di 0,0 indica il livello di fedeltà più basso possibile e 1,0 significa la massima fedeltà, che può implicare anche la perdita di perdite a seconda del codec.

CompressionQuality 0,0 indica lo schema di compressione meno efficiente disponibile, in genere con un output di codifica veloce ma di dimensioni maggiori. Il valore 1,0 indica lo schema più efficiente disponibile, che richiede in genere più tempo per la codifica, ma produce un output ridotto. A seconda delle funzionalità del codec, questo intervallo può essere mappato su un set discreto di metodi di compressione disponibili.

Lossless significa che il codec codifica l'immagine come perdita di dati senza perdita di dati dell'immagine. Se il lossless è abilitato, ImageQuality viene ignorato.

Oltre alle opzioni del codificatore generico sopra indicate, i codec forniti con WIC supportano le opzioni seguenti. Se un codec ha la necessità di supportare un'opzione coerente con l'utilizzo in questi codec forniti, è consigliabile farlo.



| Nome della proprietà           | VARTYPE           | Valore                                                                             | Codec applicabili |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | \_bool VT          | Attivato/Disattivato                                                                            | PNG               |
| FilterOption            | \_Ui1 VT           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | \_Ui1 VT           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | \_Array VT UI4/VT \_ | 64 voci (DCT)                                                                  | JPEG              |
| Chrominance             | \_Array VT UI4/VT \_ | 64 voci (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | \_Ui1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | \_bool VT          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | \_bool VT          | Attivato/Disattivato                                                                            | BMP               |



 

Usare **VT \_ vuoto** per indicare che **\* non \* è impostato** come predefinito. Se sono state impostate proprietà aggiuntive ma non supportate, il codificatore deve ignorarle; Ciò consente alle applicazioni di codificare meno logica se desiderano una funzionalità che può o non essere presente.

## <a name="encoder-options-examples"></a>Esempi di opzioni del codificatore

Nell' [esempio di codifica TIFF](#tiff-encoding-example) precedente è impostata un'opzione specifica del codificatore. Il membro *pstrName* della struttura Campo PROPBAG2 è impostato sul nome di proprietà appropriato e la variante è impostata sul VarType corrispondente e sul valore desiderato, in questo caso un membro dell'enumerazione [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Per usare le opzioni del codificatore predefinite, è sufficiente inizializzare il frame bitmap con l'elenco delle proprietà restituito al momento della creazione del frame.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



È anche possibile eliminare il contenitore delle proprietà quando non vengono prese in considerazione opzioni del codificatore.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica della decodifica](-wic-creating-decoder.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
