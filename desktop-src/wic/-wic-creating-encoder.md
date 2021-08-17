---
description: Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Cenni preliminari sulla codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee4c554046fa99cab53ff3e3acb8e2eadeb1a70a9140370dbc4b426fd576c15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088083"
---
# <a name="encoding-overview"></a>Cenni preliminari sulla codifica

Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso. L'uso di alcuni codificatori comporta compromessi, ad esempio JPEG, che scambia le informazioni sui colori per una migliore compressione. Altri codificatori non comportano perdite di questo tipo, ad esempio bitmap (BMP). Poiché molti codec usano la tecnologia proprietaria per ottenere una migliore compressione e fedeltà delle immagini, i dettagli su come viene codificata un'immagine sono a responsabilità dello sviluppatore di codec.

In questo argomento sono incluse le sezioni seguenti.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Esempio di codifica TIFF](#tiff-encoding-example)
-   [Utilizzo delle opzioni del codificatore](#encoder-options-usage)
-   [Opzioni del codificatore](#encoder-options-usage)
-   [Esempi di opzioni del codificatore](#encoder-options-examples)
-   [Argomenti correlati](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) è l'interfaccia principale per la codifica di un'immagine nel formato di destinazione e usata per serializzare i componenti di un'immagine, ad esempio thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e frame ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), nel file di immagine.

La modalità e il momento in cui viene eseguita la serializzazione vengono lasciati allo sviluppatore di codec. Ogni singolo blocco di dati all'interno del formato di file di destinazione deve essere in grado di impostare indipendentemente dall'ordine, ma anche in questo caso, questa è la decisione dello sviluppatore di codec. Dopo aver chiamato il [**metodo Commit,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) tuttavia, le modifiche all'immagine non devono essere consentite e il flusso deve essere chiuso.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode è**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) l'interfaccia per codificare i singoli fotogrammi di un'immagine. Fornisce metodi per l'impostazione di singoli componenti di creazione di immagini di fotogrammi, ad esempio anteprime e fotogrammi, nonché dimensioni dell'immagine, formati DPI e pixel.

I singoli frame possono essere codificati con metadati specifici del frame, quindi [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) fornisce l'accesso a un writer di metadati tramite il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)

Il metodo [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del frame esegue il commit di tutte le modifiche al singolo frame e indica che le modifiche a tale frame non devono più essere accettate.

## <a name="tiff-encoding-example"></a>Esempio di codifica TIFF

Nell'esempio seguente un'immagine Tagged Image File Format (TIFF) viene codificata [**usando IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). L'output TIFF viene personalizzato usando [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e il frame bitmap viene inizializzato usando le opzioni specificate. Dopo aver creato l'immagine usando [**WritePixels,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)viene eseguito il commit del frame tramite [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e l'immagine viene salvata usando [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


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
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

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

Codificatori diversi per formati diversi devono esporre opzioni diverse per la modalità di codifica di un'immagine. Windows Il componente di creazione dell'immagine (WIC) offre un meccanismo coerente per indicare se sono necessarie opzioni di codifica, consentendo comunque alle applicazioni di lavorare con più codificatori senza richiedere la conoscenza di un formato specifico. Questa operazione viene eseguita fornendo un [parametro IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) nel [**metodo CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e nel [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)

La factory dei componenti fornisce un punto di creazione semplice per la creazione di un contenitore delle proprietà delle opzioni del codificatore. I codec possono usare questo servizio se devono fornire un set semplice, intuitivo e non in conflitto di opzioni del codificatore. Il contenitore delle proprietà di creazione dell'immagine deve essere inizializzato durante la creazione con tutte le opzioni del codificatore rilevanti per tale codec. Per le opzioni del codificatore dal set canonico, l'intervallo di valori verrà applicato in Scrittura. Per esigenze più avanzate, i codec devono scrivere la propria implementazione del contenitore di proprietà.

A un'applicazione viene assegnato il contenitore delle opzioni del codificatore durante la creazione del frame e deve configurare tutti i valori prima di inizializzare il frame del codificatore. Per un'applicazione basata sull'interfaccia utente, può offrire un'interfaccia utente fissa per le opzioni del codificatore canonico e una visualizzazione avanzata per le opzioni rimanenti. Le modifiche possono essere apportate una alla volta tramite il metodo Write e qualsiasi errore verrà segnalato tramite IErrorLog. L'applicazione dell'interfaccia utente deve sempre ri-leggere e visualizzare tutte le opzioni dopo aver apportato una modifica nel caso in cui la modifica abbia causato un effetto a catena. Un'applicazione deve essere preparata per gestire l'inizializzazione dei frame non riuscita per i codec che forniscono solo la segnalazione degli errori minima tramite il proprio contenitore delle proprietà.

## <a name="encoder-options"></a>Opzioni del codificatore

Un'applicazione può prevedere che venga rilevato il set di opzioni del codificatore seguente. Le opzioni del codificatore riflettono le funzionalità di un codificatore e il formato del contenitore sottostante e pertanto non sono per loro natura realmente indipendenti dal codec. Quando possibile, le nuove opzioni devono essere normalizzate in modo che possano essere applicate ai nuovi codec che emergono.



| Nome della proprietà      | VARTYPE  | Valore                                                                     | Codec applicabili |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1.0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1.0                                                                     | TIFF              |
| Lossless           | VT \_ BOOL | **TRUE,** **FALSE**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty di 0,0 indica la fedeltà più bassa possibile e 1.0 indica la massima fedeltà, che può anche implicare perdita a seconda del codec.

CompressionQuality di 0,0 indica lo schema di compressione meno efficiente disponibile, che in genere comporta una codifica veloce ma un output più grande. Il valore 1.0 indica lo schema più efficiente disponibile, in genere richiede più tempo per la codifica, ma produce un output più piccolo. A seconda delle funzionalità del codec, questo intervallo può essere mappato a un set discreto di metodi di compressione disponibili.

Senza perdita significa che il codec codifica l'immagine come senza perdita di dati senza perdita di dati dell'immagine. Se Lossless è abilitato, ImageQuality viene ignorato.

Oltre alle opzioni del codificatore generico precedenti, i codec forniti con WIC supportano le opzioni seguenti. Se un codec deve supportare un'opzione coerente con l'utilizzo di questi codec forniti, è consigliato farlo.



| Nome della proprietà           | VARTYPE           | Valore                                                                             | Codec applicabili |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ BOOL          | Attivato/Disattivato                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/VT \_ ARRAY | 64 voci (DCT)                                                                  | JPEG              |
| Chrominance             | VT \_ UI4/VT \_ ARRAY | 64 voci (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ BOOL          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ BOOL          | Attivato/Disattivato                                                                            | BMP               |



 

Usare **VT \_ EMPTY** per indicare **\* che non è impostato \*** come predefinito. Se le proprietà aggiuntive sono impostate ma non supportate, il codificatore deve ignorarle. ciò consente alle applicazioni di codificare meno logica se vogliono una funzionalità che può o meno essere presente.

## <a name="encoder-options-examples"></a>Esempi di opzioni del codificatore

[Nell'esempio di codifica TIFF precedente](#tiff-encoding-example) è impostata un'opzione del codificatore specifica. Il *membro pstrName* della struttura PROPBAG2 viene impostato sul nome della proprietà appropriato e VARIANT viene impostato sul VARTYPE corrispondente e sul valore desiderato, in questo caso un membro dell'enumerazione [**WICTiffCompressionOption.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)


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



Per usare le opzioni predefinite del codificatore, è sufficiente inizializzare il frame bitmap con il contenitore delle proprietà restituito al momento della creazione del frame.


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



È anche possibile eliminare il contenitore delle proprietà quando non vengono considerate opzioni del codificatore.


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

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica della decodifica](-wic-creating-decoder.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
