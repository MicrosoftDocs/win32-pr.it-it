---
description: Synchronized Accessible Media Interchange (SAMI) è un formato per l'aggiunta di sottotitoli ai supporti digitali.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Origine supporti SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7567f7479b6f8d0d2439f89dbf3e6cf273fc7dcae31590ddf9b51a4d66a6940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034819"
---
# <a name="sami-media-source"></a>Origine supporti SAMI

Synchronized Accessible Media Interchange (SAMI) è un formato per l'aggiunta di sottotitoli ai supporti digitali. Le didascalie vengono archiviate in un file di testo separato con estensione smi o sami.

In Media Foundation, i file di sottotitoli SAMI sono supportati tramite l'origine multimediale SAMI. Usare il [sistema di risoluzione dell'origine](source-resolver.md) per creare un'istanza dell'origine multimediale SAMI da un URL o un flusso di byte. Media Foundation non fornisce un componente che visualizza i sottotitoli SAMI. L'applicazione deve interpretare i dati dei sottotitoli ricevuti dall'origine multimediale SAMI.

Di seguito viene illustrato un file SAMI di esempio.

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

`<STYLE>`L'elemento contiene informazioni sullo stile. Questo esempio contiene uno stile di base per `<P>` gli elementi, insieme a due stili denominati, "standard" e "hilite". Gli stili denominati vengono usati per modificare lo stile di base. Le didascalie vengono inserite all'interno `<SYNC>` degli elementi. L'attributo start indica il tempo di presentazione in millisecondi per la didascalia. Le didascalie in questo esempio sono fornite in due lingue, specificate dai tag di lingua RFC-1766, "en-US" e "fr -FR". All'interno delle didascalie, le lingue sono identificate dai relativi nomi di classe. in questo caso, "ENUSCC" e "FRFRCC".

L'origine multimediale SAMI crea un flusso multimediale per ogni lingua. Per impostazione predefinita, il primo flusso è selezionato e i flussi rimanenti vengono deselezionati. L'applicazione può modificare la selezione del flusso chiamando [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Ogni descrittore di flusso contiene gli attributi seguenti.



| Attributo                                                       | Descrizione                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**LINGUAGGIO \_ MF SD \_**](mf-sd-language-attribute.md)            | Tag di lingua, come specificato `lang` dall'attributo .  |
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Nome della lingua, come specificato `Name` dall'attributo . |



 

Ogni flusso ha il tipo di supporto seguente:



| Attributo                                                                            | Valore                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                            | **MFMediaType \_ SAMI** |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

L'origine SAMI recapita ogni didascalia in un esempio di supporto separato. Il timestamp e la durata di esempio derivano `<SYNC>` dall'elemento . Il buffer multimediale contenuto nell'esempio contiene la didascalia come testo ASCII. Lo stile della didascalia viene incorporato nella didascalia come attributo `STYLE` inline. Ad esempio, dato il file SAMI precedente e l'uso del flusso in lingua inglese con gli stili predefiniti, il primo buffer multimediale conterrà i dati seguenti. Le interruzioni di riga potrebbero essere diverse da quanto illustrato di seguito.

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Stili SAMI

Per modificare lo stile corrente, usare [**l'interfaccia IMFSAMIStyle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) Questa interfaccia viene ottenuta chiamando [**IMFGetService::GetService sull'origine**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) dei supporti SAMI. Se si usa l'origine multimediale SAMI con la sessione multimediale, chiamare **GetService** nella sessione multimediale. L'identificatore del servizio **è MF \_ SAMI \_ SERVICE.**

Nell'esempio seguente viene impostato lo stile SAMI corrente, specificato da index.


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



Questo esempio chiama i metodi seguenti sull'origine multimediale SAMI:

-   [**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) ottiene il numero di stili.
-   [**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) ottiene un elenco dei nomi di stile, archiviati in **un oggetto PROPVARIANT.**
-   [**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) imposta uno stile in base al nome.

L'elenco di nomi di stile viene archiviato anche nel descrittore di presentazione, nell'attributo [**\_ \_ SAMI \_ STYLELIST di MF PD.**](mf-pd-sami-stylelist-attribute.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini multimediali e sink](media-sources-and-sinks.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



