---
description: Visualizzazione di didascalie chiuse
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Visualizzazione di didascalie chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558056"
---
# <a name="viewing-closed-captions"></a>Visualizzazione di didascalie chiuse

Per supportare le didascalie chiuse nella televisione analoga, il filtro di acquisizione espone un pin che recapita i dati di VBI o della didascalia chiusa. Il pin avrà una delle categorie di pin seguenti:

-   Pin VBI (PIN \_ Category \_ VBI). Fornisce un flusso di esempi di forma d'onda VBI. Questi vengono passati a un filtro decodificatore che estrae i dati di didascalia chiusi.
-   Pin CC ( \_ categoria pin \_ CC). Recapita le coppie di byte con didascalia chiusa, estratti dai dati riga 21.
-   Hardware slicing CC pin (PINNAME \_ video \_ CC \_ Capture).

Per visualizzare in anteprima le didascalie chiuse, chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoria pin VBI e, in caso di errore, richiamarla con la categoria CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



Il diagramma seguente illustra un tipico grafico di filtro per la visualizzazione di didascalie chiuse.

![grafico di anteprima sottotitoli codificati](images/vidcap08.png)

Questo grafico usa i filtri seguenti per la visualizzazione dei sottotitoli chiusi:

-   [Convertitore da tee a sink a sink](tee-sink-to-sink-converter.md). Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi distinti per ognuno dei servizi dati presenti sul segnale. Microsoft fornisce codec VBI per la didascalia chiusa, NABTS e il televideo internazionale (WST).
-   [Decodificatore CC](cc-decoder-filter.md). Decodifica i dati CC dalle forme d'onda VBI campionate fornite dal filtro di acquisizione.
-   [Decodificatore riga 21](line-21-decoder-filter.md). Converte le coppie di byte CC e disegna il testo della didascalia sulle bitmap. Il filtro downstream (in questo caso il mixer overlay) sovrappone le bitmap nel video.

Il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generatore di grafici di acquisizione aggiunge questi filtri automaticamente. Se il filtro di acquisizione ha un pin CC anziché un pin VBI, il pin CC viene connesso direttamente al filtro decodificatore riga 21.

> [!Note]  
> Se si usa il filtro VMR (video Mixing Renderer) per il rendering, usare il filtro decodificatore riga 21 2. Questo filtro ha la stessa funzionalità del decodificatore della riga 21, ma il CLSID è CLSID \_ Line21Decoder2.

 

> [!Note]  
> Il filtro del decodificatore CC è stato rimosso in Windows Vista. Le nuove applicazioni devono usare il filtro VBICodec, documentato nella documentazione relativa alle tecnologie Microsoft TV.

 

Se il dispositivo di acquisizione usa una porta video, il filtro di acquisizione potrebbe avere una porta video VBI pin (PIN \_ Category \_ VIDEOPORT \_ VBI). Questo pin deve essere connesso al filtro [VBI Surface allocator](vbi-surface-allocator.md) , che alloca le superfici in modo da contenere i dati VBI acquisiti. Il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge questo filtro se necessario. Il diagramma seguente mostra un grafico di filtro con l'allocatore della superficie di VBI.

![grafico di anteprima dei sottotitoli codificati con VBI Surface allocator](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Abilitazione e disabilitazione delle didascalie

Per controllare la visualizzazione dei sottotitoli, usare l'interfaccia [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) sul filtro del decodificatore della riga 21. Ad esempio, è possibile disattivare la visualizzazione didascalia usando il metodo [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , come indicato di seguito:


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



Questo esempio usa il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per individuare l'interfaccia [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) . Il primo parametro di **FindInterface** è **&cercare \_ \_ solo downstream**, che specifica la ricerca a valle dal filtro di acquisizione (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Acquisizione di bitmap didascalia chiuse

È possibile acquisire le bitmap della didascalia in un file. A tale scopo, aggiungere la sezione relativa alla scrittura di file del grafico di filtro, come descritto in [acquisizione di video in un file](capturing-video-to-a-file.md). Eseguire quindi il rendering del pin CC o VBI nel filtro Mux:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Se si sta acquisendo anche il video, verrà creato un file con due flussi video distinti. Il video non verrà acquisito con le didascalie sovrapposte sopra l'immagine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Didascalie e televideo chiusi](closed-captions-and-teletext.md)
</dt> </dl>

 

 



