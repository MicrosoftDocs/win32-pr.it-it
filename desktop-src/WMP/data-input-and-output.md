---
title: Dati di input e di output
description: Dati di input e di output
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player plug-in, input e output dei dati
- plug-in, input e output dei dati
- plug-in di elaborazione del segnale digitale, input e output dei dati
- Plug-in DSP, input e output dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31e7c6fba24451d65e59c3fb9f56ec6b1413be3d595530414c25c52964b9b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863671"
---
# <a name="data-input-and-output"></a>Dati di input e di output

Windows Media Player dati audio o video ai plug-in DSP tramite un buffer di input allocato da Windows Media Player. I plug-in DSP restituiscono i dati elaborati Windows Media Player tramite un buffer di output allocato anche da Windows Media Player. Windows Media Player il processo di passaggio dei dati tra se stesso e il plug-in DSP chiamando i metodi implementati dal plug-in. Per un plug-in che funge da oggetto multimediale DirectX (DMO), il processo funziona come segue:

1.  Windows Media Player chiama **IMediaObject::P rocessInput**, passando un puntatore a un **oggetto IMediaBuffer** al plug-in DSP.
2.  Il plug-in DSP mantiene un conteggio dei riferimenti sull'oggetto buffer di input. Il plug-in DSP restituisce un HRESULT di esito positivo o **negativo appropriato.**
3.  Windows Media Player chiama **IMediaObject::P rocessOutput**, passando un puntatore a una matrice di strutture BUFFER DI **\_ OUTPUT \_ DATA \_ di DMO** (che contengono buffer di output) al plug-in DSP.
4.  Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato. Il plug-in DSP rilascia il conteggio dei riferimenti sull'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati. Il plug-in DSP restituisce quindi un HRESULT di esito positivo o **negativo appropriato.**
5.  Windows Media Player esegue il rendering del contenuto nel buffer di output.

Per un plug-in che funge da Media Foundation Transform (MFT), il processo funziona come segue:

-   Windows Media Player chiama **IMFTransform::P rocessInput**, passando un puntatore a un oggetto interfaccia **IMFSample** al plug-in DSP.
    1.  Il plug-in DSP mantiene un conteggio dei riferimenti **sull'interfaccia IMFSample.** Il plug-in DSP restituisce un HRESULT di esito positivo o **negativo appropriato.**
    2.  Windows Media Player chiama **IMFTransform::P rocessOutput**, passando un puntatore a una matrice di strutture **MFT \_ OUTPUT DATA \_ \_ BUFFER** (che contengono buffer di output) al plug-in DSP.
    3.  Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato. Il plug-in DSP rilascia il conteggio dei riferimenti sull'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati. Il plug-in DSP restituisce quindi un HRESULT di esito positivo o **negativo appropriato.**
    4.  Windows Media Player esegue il rendering del contenuto nel buffer di output.

Questo processo si ripete continuamente mentre il plug-in è abilitato e Windows Media Player contenuto di cui eseguire il rendering.

> [!Note]  
> Non scrivere codice che scrive dati nel buffer di input o legge i dati dal buffer di output. L'accesso non corretto ai buffer di dati può produrre risultati imprevisti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




