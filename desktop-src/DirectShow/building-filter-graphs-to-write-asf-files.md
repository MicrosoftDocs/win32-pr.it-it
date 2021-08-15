---
description: Compilazione di grafici filtro per la scrittura di file ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Compilazione di grafici filtro per la scrittura di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe53dcee310be34c321dfc2e988807184735a24b0793d68e3ca7dea10d0b29e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662751"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Compilazione di grafici filtro per la scrittura di file ASF

Quando si Windows contenuto basato su supporti, le applicazioni usano in genere uno degli scenari seguenti:

-   Conversione o transcoding di contenuto da un altro formato Windows media.
-   Inserimento di contenuto non Windows basato su supporti (formati di flusso nativi) nei file ASF.
-   Acquisizione di dati in tempo reale e codifica immediatamente in Windows media.

Transcodificare i file ASF

È possibile compilare un grafico di filtro di transcodificare file usando [WM ASF Writer](wm-asf-writer-filter.md) in vari modi. Il modo più semplice è aggiungere WM ASF Writer al grafico dei filtri e quindi usare il metodo IGraphBuilder::RenderFile per compilare automaticamente il grafo.

Un modo alternativo consiste nell'aggiungere manualmente ogni filtro al grafico e connettere i segnaposto. Dopo aver aggiunto WM ASF Writer, configurarlo usando i metodi IConfigAsfWriter se il profilo predefinito non è appropriato e connettere i pin di input di WM ASF Writer ai pin di output corrispondenti nei filtri upstream.

La figura seguente illustra le configurazioni tipiche del filtro di transcodificare WM ASF Writer.

![Grafico dei filtri di transcoding](images/asf-transcode.png)

Inserimento di formati di flusso nativi nei file ASF

Per impostazione predefinita, il filtro WM ASF Writer prevede flussi audio e video non compressi sui pin di input e usa i codec Windows Media Audio e Windows Media Video per comprimere i flussi. Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati. Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e DRM (Digital Rights Management), senza dover transcodificare il contenuto.

Per creare un file ASF che contiene contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico di filtro a monte di WM ASF Writer e ignorare il meccanismo di compressione di WM ASF Writer chiamando [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) come segue:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Configurare quindi il filtro con il profilo desiderato. È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo. In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato in modo che corrisponda.

Quando si connette WM ASF Writer al filtro upstream, usare il metodo IGraphBuilder::ConnectDirect. Non usare metodi di "connessione intelligente", ad esempio IGraphBuilder::Connessione o IGraphBuilder::RenderFile per connettere il filtro, perché in questo modo verrà disabilitata la modalità di "compressione bypass" del filtro.

Acquisizione diretta da un dispositivo a un file ASF

Quando si acquisiscono audio o video direttamente in un file ASF, il grafico dei filtri sarà simile al seguente, a seconda del tipo di dispositivo di acquisizione usato.

![Grafico di acquisizione video di Windows Media](images/asf-webcam.png)

Per altre informazioni sulla creazione di grafici di acquisizione video e audio, vedere gli argomenti seguenti:

-   [Acquisizione audio](audio-capture.md)
-   [Acquisizione video](video-capture.md)

WM ASF Writer non verrà eseguito a meno che non siano connessi tutti i relativi pin. Se si configura WM ASF Writer con il profilo di sistema predefinito (scelta non consigliata) o qualsiasi profilo con flussi audio e video, verrà creato un pin di input per ogni flusso e ognuno di questi pin deve essere connesso. Se ad esempio non si intende acquisire l'audio, assicurarsi di configurare il filtro con un profilo solo video in modo che non sia stato creato alcun pin audio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



