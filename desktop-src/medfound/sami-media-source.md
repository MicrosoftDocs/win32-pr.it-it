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
# <a name="sami-media-source"></a>Origine supporto SAMI

Il formato SAMI (Synchronized Accessible Media Interchange) è un formato per l'aggiunta di didascalie ai supporti digitali. Le didascalie vengono archiviate in un file di testo separato con estensione SMI o Sami.

In Media Foundation i file di didascalia SAMI sono supportati tramite l'origine dei supporti SAMI. Usare il [resolver di origine](source-resolver.md) per creare un'istanza dell'origine supporto Sami da un URL o un flusso di byte. Media Foundation non fornisce un componente che visualizza le didascalie SAMI. L'applicazione deve interpretare i dati della didascalia ricevuti dall'origine dei supporti SAMI.

Di seguito viene illustrato un esempio di file SAMI.

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

L' `<STYLE>` elemento contiene informazioni sullo stile. Questo esempio contiene uno stile di base per `<P>` gli elementi, insieme a due stili denominati, "standard" e "Hilite". Gli stili denominati vengono utilizzati per modificare lo stile di base. Le didascalie vengono posizionate all'interno di `<SYNC>` elementi. L'attributo Start restituisce il tempo di presentazione in millisecondi per la didascalia. Le didascalie di questo esempio sono fornite in due lingue, specificate dai tag di lingua RFC-1766, "en-US" e "fr-FR". All'interno delle didascalie, le lingue sono identificate dai rispettivi nomi di classe; in questo caso, "ENUSCC" e "FRFRCC".

L'origine dei supporti SAMI crea un flusso multimediale per ogni lingua. Per impostazione predefinita, il primo flusso è selezionato e i flussi rimanenti vengono deselezionati. L'applicazione può modificare la selezione del flusso chiamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Ogni descrittore di flusso contiene gli attributi seguenti.



| Attributo                                                       | Descrizione                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**\_lingua MF SD \_**](mf-sd-language-attribute.md)            | Tag di lingua, come specificato dall' `lang` attributo.  |
| [**\_lingua MF SD \_ Sami \_**](mf-sd-sami-language-attribute.md) | Nome del linguaggio, come specificato dall' `Name` attributo. |



 

Ogni flusso ha il seguente tipo di supporto:



| Attributo                                                                            | Valore                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                            | **\_Sami MFMediaType** |
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

L'origine SAMI recapita ogni didascalia in un esempio di supporto separato. Il timestamp e la durata del campione sono derivati dall' `<SYNC>` elemento. Il buffer multimediale contenuto nell'esempio contiene la didascalia come testo ASCII. Lo stile della didascalia viene incorporato nella didascalia come attributo inline `STYLE` . Ad esempio, dato il file SAMI precedente e usando il flusso della lingua inglese con gli stili predefiniti, il primo buffer multimediale conterrebbe i dati seguenti. (Le interruzioni di riga potrebbero essere diverse da quelle illustrate qui).

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

Per modificare lo stile corrente, utilizzare l'interfaccia [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) . Questa interfaccia viene ottenuta chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sull'origine dei supporti Sami. Se si usa l'origine del supporto SAMI con la sessione multimediale, chiamare **GetService** nella sessione multimediale. L'identificatore del servizio è il **\_ \_ servizio MF Sami**.

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



Questo esempio chiama i metodi seguenti nell'origine supporto SAMI:

-   [**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) ottiene il numero di stili.
-   [**IMFSAMIStyle:: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) ottiene un elenco dei nomi di stile, archiviati in un **PROPVARIANT**.
-   [**IMFSAMIStyle:: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) imposta uno stile in base al nome.

L'elenco dei nomi di stile viene archiviato anche nel descrittore della presentazione, nell'attributo di stile dell'elenco di [**\_ \_ \_ stili MF PD Sami**](mf-pd-sami-stylelist-attribute.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini e sink multimediali](media-sources-and-sinks.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



