---
title: Dati di input e di output
description: Dati di input e di output
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-in di Windows Media Player, input e output dei dati
- plug-in, input e output dei dati
- plug-in per l'elaborazione di segnali digitali, input e output dei dati
- Plug-in DSP, input e output dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116837"
---
# <a name="data-input-and-output"></a>Dati di input e di output

Windows Media Player fornisce dati audio o video a plug-in DSP tramite un buffer di input allocato da Windows Media Player. I plug-in DSP restituiscono i dati elaborati a Windows Media Player tramite un buffer di output anch ' esso allocato da Windows Media Player. Windows Media Player gestisce il processo di passaggio dei dati tra se stesso e il plug-in DSP chiamando i metodi implementati dal plug-in. Per un plug-in che agisce come DMO (DirectX Media Object), il processo funziona nel modo seguente:

1.  Windows Media Player chiama **IMediaObject::P rocessinput**, passando un puntatore a un oggetto **IMediaBuffer** al plug-in DSP.
2.  Il plug-in DSP mantiene un conteggio dei riferimenti nell'oggetto buffer di input. Il plug-in DSP restituisce un **HRESULT** di esito positivo o negativo appropriato.
3.  Windows Media Player chiama **IMediaObject::P rocessoutput**, passando un puntatore a una matrice di strutture del **\_ \_ \_ buffer dei dati di output DMO** , che contengono buffer di output, al plug-in DSP.
4.  Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato. Il plug-in DSP rilascia il conteggio dei riferimenti nell'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati. Il plug-in DSP restituisce quindi un **HRESULT** di esito positivo o negativo appropriato.
5.  Windows Media Player esegue il rendering del contenuto nel buffer di output.

Per un plug-in che agisce come una trasformazione Media Foundation (MFT), il processo funziona nel modo seguente:

-   Windows Media Player chiama **IMFTransform::P rocessinput**, passando un puntatore a un oggetto di interfaccia **IMFSample** al plug-in DSP.
    1.  Il plug-in DSP mantiene un conteggio dei riferimenti nell'interfaccia **IMFSample** . Il plug-in DSP restituisce un **HRESULT** di esito positivo o negativo appropriato.
    2.  Windows Media Player chiama **IMFTransform::P rocessoutput**, passando un puntatore a una matrice di strutture del **\_ \_ \_ buffer dei dati di output di MFT** (che contengono buffer di output) al plug-in DSP.
    3.  Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato. Il plug-in DSP rilascia il conteggio dei riferimenti nell'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati. Il plug-in DSP restituisce quindi un **HRESULT** di esito positivo o negativo appropriato.
    4.  Windows Media Player esegue il rendering del contenuto nel buffer di output.

Questo processo si ripete continuamente quando il plug-in è abilitato e Windows Media Player dispone di contenuto di cui eseguire il rendering.

> [!Note]  
> Non scrivere codice che scrive i dati nel buffer di input o legge i dati dal buffer di output. L'accesso non corretto ai buffer dei dati può produrre risultati imprevisti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




