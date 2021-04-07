---
description: Filtro muxer DV
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro muxer DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747399"
---
# <a name="dv-muxer-filter"></a>Filtro muxer DV

Questo filtro combina un flusso video codificato Digital video (DV) con uno o due flussi audio per produrre un flusso DV con interfoliazione. Per scrivere il flusso in un file AVI, connettere il filtro al filtro [Mux AVI](avi-mux-filter.md) e connettere il *Mux AVI* al filtro del [writer di file](file-writer-filter.md) . Per altre informazioni, vedere [video digitale in DirectShow](digital-video-in-directshow.md).



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Tipi di supporti pin di input                    | **Video**: MEDIATYPE \_ video, MEDIASUBTYPE \_ DVSD, Format \_ videoinfo **audio**: MEDIATYPE \_ audio, MEDIASUBTYPE \_ PCM, Format \_ WAVEFORMATEX |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Tipi di supporti pin di output                   | MEDIATYPE con \_ interfoliazione, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo                                                                             |
| Interfacce del PIN di output                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| CLSID filtro                             | \_DVMUX CLSID                                                                                                                           |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                       |
| File eseguibile                               | qdv.dll                                                                                                                                |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                                                        |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il muxer DV può creare due pin di input audio. Supporta i formati audio indicati nella tabella seguente.



Pin audio 1

Pin audio 2

Formato output

Frequenza di campionamento (kHz)

BITS/esempio

Canali

Frequenza di campionamento

BITS/esempio

Canali

32

16

Mono

Non connesso

Canale SD 2

32

16

Stereo

Non connesso

Canale SD 4

44,1 o 48

16

Stereo o mono

Non connesso

Canale SD 2

Non connesso

32

16

Stereo o mono

Non consentita

Non connesso

44,1 o 48

16

Mono

Non consentita

Non connesso

44,1 o 48

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

Stereo o mono\*

32

16

Stereo o mono\*

Canale SD 4

44,1

16

Mono

44,1

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



 

Ai fini di questa tabella, il pin audio 1 viene definito come primo pin di input connesso a un'origine audio e il pin audio 2 viene definito come il secondo pin di input connesso a un'origine audio. Una volta connesso un pin audio, questo schema di numerazione rimane attivo, a meno che entrambi i pin audio non siano disconnessi. Ad esempio, se si connettono entrambi i pin audio e si disconnette il pin audio 1, il pin rimanente verrà ancora considerato pin 2.

L'audio fornito al pin 1 viene registrato nel primo blocco audio dei frame DV (CH1) e l'audio fornito al pin 2 viene registrato nel secondo blocco audio (CH2). Eccezione: se il filtro ha un singolo input stereo a 44,1 kHz o 48 kHz, il canale audio sinistro viene registrato nel primo blocco audio e il canale audio destro viene registrato nel secondo blocco audio.

Per l'output del canale SD 4: se l'input è stereo, il tracciato a sinistra viene registrato in CHa o CHc e la traccia corretta viene registrata in CHb o CHd. Se l'input è mono, l'audio viene registrato in CHa o CHc e CHb e CHd sono invisibili.

Con la connessione e la disconnessione del pin audio 1, è possibile raggiungere un formato non consentito. In tal caso, il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro restituisce VFW \_ E \_ non \_ connesso. Questa limitazione impedisce una situazione in cui il primo blocco audio non dispone di audio, ma il secondo blocco audio dispone di audio. Il secondo blocco deve avere audio solo se il primo blocco include anche audio.

Il muxer DV non consente input audio con frequenze di campionamento diverse. Tuttavia, i metodi per la creazione di grafici, ad esempio [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , aggiungono in genere il filtro del [wrapper ACM](acm-wrapper-filter.md) , che converte il secondo flusso audio in modo che corrisponda alla frequenza di campionamento del primo flusso.

Se l'input audio è 48 kHz o 32 kHz, l'output audio è bloccato. Non è possibile bloccare l'audio a 44,1 kHz.

Se non è connesso alcun pin audio, l'output contiene i dati audio dei frame DV in arrivo. Potrebbe trattarsi di un silenzio o di dati audio validi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



