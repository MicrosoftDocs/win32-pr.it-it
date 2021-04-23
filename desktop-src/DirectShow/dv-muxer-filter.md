---
description: Filtro DV Muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro DV Muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908599"
---
# <a name="dv-muxer-filter"></a>Filtro DV Muxer

Questo filtro combina un flusso video codificato DV (Digital Video) con uno o due flussi audio per produrre un flusso DV interleaved. Per scrivere il flusso in un file AVI, connettere questo filtro al filtro [Mux AVI](avi-mux-filter.md) e connettere *mux AVI* al filtro [Writer file.](file-writer-filter.md) Per altre informazioni, vedere [Video digitale in DirectShow.](digital-video-in-directshow.md)



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Tipi di supporti pin di input                    | **Video:** MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                             |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| Filtro CLSID                             | CLSID \_ DVMux                                                                                                                           |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                       |
| File eseguibile                               | qdv.dll                                                                                                                                |
| [Merito](merit.md)                       | MERITO \_ IMPROBABILE                                                                                                                        |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il DV Muxer può creare due pin di input audio. Supporta i formati audio illustrati nella tabella seguente.



Pin audio 1

Pin audio 2

Formato output

Frequenza di campionamento (kHz)

Bit/esempio

Canali

Frequenza di campionamento

Bit/esempio

Canali

32

16

Mono

Estraneo

Canale SD 2

32

16

Stereo

Estraneo

Canale SD 4

44.1 o 48

16

Stereo o Mono

Estraneo

Canale SD 2

Estraneo

32

16

Stereo o Mono

Non consentita

Estraneo

44.1 o 48

16

Mono

Non consentita

Estraneo

44.1 o 48

16

Stereo

Canale SD 2

32

16

Mono

32

16

Mono

Canale SD 2

32

16

Stereo o Mono\*

32

16

Stereo o Mono\*

Canale SD 4

44.1

16

Mono

44.1

16

Mono

Canale SD 2

48

16

Mono

48

16

Mono

Canale SD 2

\* Se almeno un pin di input è stereo.



 

Ai fini di questa tabella, il pin audio 1 viene definito come primo pin di input connesso a un'origine audio e il pin audio 2 viene definito come secondo pin di input connesso a un'origine audio. Una volta connesso un pin audio, questo schema di numerazione rimane attivo a meno che entrambi i pin audio non siano disconnessi. Ad esempio, se si connettono entrambi i pin audio e quindi si disconnette il pin audio 1, il pin rimanente viene comunque considerato pin 2.

L'audio fornito al pin 1 viene registrato nel primo blocco audio dei fotogrammi DV (CH1) e l'audio fornito al pin 2 viene registrato nel secondo blocco audio (CH2). Eccezione: se il filtro ha un singolo input stereo a 44,1 kHz o 48 kHz, il canale audio sinistro viene registrato nel primo blocco audio e il canale audio destro viene registrato nel secondo blocco audio.

Per l'output SD a 4 canali: se l'input è stereo, la traccia sinistra viene registrata in CHa o CHc e la traccia destra viene registrata in CHb o CHd. Se l'input è mono, l'audio viene registrato in CHa o CHc e CHb e CHd sono invisibile all'utente.

Connettendo e disconnettendo il pin audio 1, è possibile raggiungere un formato non consentito. In tal caso, il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro restituisce VFW \_ E NOT \_ \_ CONNECTED. Questa limitazione impedisce una situazione in cui il primo blocco audio non ha audio, ma il secondo blocco audio dispone di audio. Il secondo blocco deve avere audio solo se anche il primo blocco dispone di audio.

Il DV Muxer non consente input audio con frequenze di campionamento diverse. Tuttavia, i metodi di creazione di grafi, ad esempio [**IGraphBuilder::Connect,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) in genere aggiungono il filtro [wrapper ACM,](acm-wrapper-filter.md) che converte il secondo flusso audio in modo che corrisponda alla frequenza di campionamento del primo flusso.

Se l'input audio è di 48 kHz o 32 kHz, l'output audio viene bloccato. Non è possibile bloccare l'audio a 44,1 kHz.

Se non sono connessi pin audio, l'output contiene i dati audio dai fotogrammi DV in ingresso. Potrebbe trattarsi di un silenzio o di dati audio validi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



