---
description: Visualizzazione di sottotitoli codificati
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Visualizzazione di sottotitoli codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903433"
---
# <a name="viewing-closed-captions"></a>Visualizzazione di sottotitoli codificati

Per supportare i sottotitoli codificati nella tv analogica, il filtro di acquisizione espone un segnaposto che recapita dati VBI o sottotitoli codificati. Il pin avrà una delle categorie di pin seguenti:

-   VBI pin (PIN \_ CATEGORY \_ VBI). Fornisce un flusso di esempi di forme d'onda VBI. Questi vengono passati a un filtro decodificatore che estrae i dati dei sottotitoli codificati.
-   CC pin (PIN \_ CATEGORY \_ CC). Recapita coppie di byte con sottotitoli codificati, estratte dai dati della riga 21.
-   Pin CC di sezione hardware (PINNAME \_ VIDEO \_ CC \_ CAPTURE).

Per visualizzare l'anteprima dei sottotitoli codificati, chiamare [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoria di pin VBI e, in caso di errore, chiamarlo nuovamente con la categoria CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



Il diagramma seguente illustra un grafico di filtro tipico per la visualizzazione di sottotitoli codificati.

![grafico di anteprima dei sottotitoli codificati](images/vidcap08.png)

Questo grafico usa i filtri seguenti per la visualizzazione dei sottotitoli codificati:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi separati per ognuno dei servizi dati presenti nel segnale. Microsoft fornisce codec VBI per sottotitoli codificati, NABTS e WST (World Standard Teletext).
-   [Decodificatore CC](cc-decoder-filter.md). Decodifica i dati CC dalle forme d'onda VBI campionate fornite dal filtro di acquisizione.
-   [Decodificatore di riga 21.](line-21-decoder-filter.md) Converte le coppie di byte CC e disegna il testo della didascalia in bitmap. Il filtro downstream (in questo caso il filtro Overlay Mixer) sovrappone le bitmap al video.

Il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Graph Capture di Builder aggiunge automaticamente questi filtri. Se il filtro di acquisizione ha un pin CC invece di un pin VBI, il pin CC è connesso direttamente al filtro del decodificatore Line 21.

> [!Note]  
> Se si usa il filtro Video Mixing Renderer (VMR) per il rendering, usare il filtro decodificatore line 21 2. Questo filtro ha la stessa funzionalità del decodificatore Line 21, ma il CLSID è CLSID \_ Line21Decoder2.

 

> [!Note]  
> Il filtro CC Decoder è stato rimosso in Windows Vista. Le nuove applicazioni devono usare il filtro VBICodec, documentato nella documentazione di Microsoft TV Technologies.

 

Se il dispositivo di acquisizione usa una porta video, il filtro di acquisizione potrebbe avere un pin VBI della porta video (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Questo pin deve essere connesso al filtro [VBI Surface Allocator,](vbi-surface-allocator.md) che alloca le superfici per contenere i dati VBI acquisiti. Il [**metodo RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge questo filtro, se necessario. Il diagramma seguente illustra un grafo di filtro con l'allocatore di superficie VBI.

![grafico di anteprima dei sottotitoli codificati con l'allocatore di superficie vbi](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Abilitazione e disabilitazione dei sottotitoli

Per controllare la visualizzazione dei sottotitoli, usare [**l'interfaccia IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) nel filtro decodificatore Line 21. Ad esempio, è possibile disattivare la visualizzazione dei sottotitoli usando il metodo [**IAMLine21Decoder::SetServiceState,**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) come indicato di seguito:


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



Questo esempio usa il [**metodo ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per individuare [**l'interfaccia IAMLine21Decoder.**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) Il primo parametro di **FindInterface** è **&LOOK \_ DOWNSTREAM \_ ONLY**, che specifica di eseguire la ricerca a valle dal filtro di acquisizione (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Acquisizione di bitmap di sottotitoli codificati

È possibile acquisire le bitmap della didascalia in un file. A tale scopo, aggiungere la sezione di scrittura di file del grafico dei filtri, come descritto in [Acquisizione di video in un file](capturing-video-to-a-file.md). Eseguire quindi il rendering del pin CC o VBI al filtro mux:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Se si acquisisce anche il video, verrà creato un file con due flussi video separati. Non acquisisce il video con didascalie sovrapposte all'immagine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottotitoli codificati e teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



