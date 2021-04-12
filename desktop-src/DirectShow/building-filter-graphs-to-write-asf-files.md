---
description: Creazione di grafici filtro per la scrittura di file ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Creazione di grafici filtro per la scrittura di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482269"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Creazione di grafici filtro per la scrittura di file ASF

Quando si crea contenuto basato su Windows Media, le applicazioni usano in genere uno degli scenari seguenti:

-   Conversione o transcodifica del contenuto da un altro formato in formato Windows Media.
-   Inserimento di contenuto non basato su Windows Media (formati di flusso nativo) in file ASF.
-   Acquisizione dei dati in tempo reale e codifica immediata nel formato Windows Media.

Transcodifica di file ASF

È possibile creare un grafico di filtro per la transcodifica di file usando il [writer ASF WM](wm-asf-writer-filter.md) in diversi modi. Il modo più semplice consiste nell'aggiungere il writer ASF WM al grafico di filtro e quindi usare il metodo IGraphBuilder:: RenderFile per creare automaticamente il grafo.

In alternativa, è possibile aggiungere manualmente ogni filtro al grafico e connettere i pin. Dopo aver aggiunto il writer WM ASF, configurarlo usando i metodi IConfigAsfWriter se il profilo predefinito non è adatto e connettere i pin di input del writer ASF WM ai pin di output corrispondenti nei filtri upstream.

Nella figura seguente viene illustrata la tipica configurazione del grafico di filtro per la transcodifica del writer WM ASF.

![transcodifica del grafico filtro](images/asf-transcode.png)

Inserimento di formati di flusso nativi in file ASF

Per impostazione predefinita, il filtro di scrittura WM ASF prevede flussi audio e video non compressi nei pin di input e usa i codec Windows Media Audio e Windows Media Video per comprimere i flussi. Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati. Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e Digital Rights Management (DRM), senza la necessità di transcodificare il contenuto.

Per creare un file ASF che contiene contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico del filtro a Monte del writer ASF WM e ignorare il meccanismo di compressione del writer ASF WM chiamando [**IConfigAsfWriter2:: separat**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) nel modo seguente:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Configurare quindi il filtro con il profilo desiderato. È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo. In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato per la corrispondenza.

Quando si connette il writer ASF WM al filtro upstream, usare il metodo IGraphBuilder:: ConnectDirect. Non usare alcun metodo di "connessione intelligente", ad esempio IGraphBuilder:: Connect o IGraphBuilder:: RenderFile per connettere il filtro in quanto questa operazione Disabilita la modalità "bypass Compression" del filtro.

Acquisizione diretta da un dispositivo a un file ASF

Quando si acquisisce audio o video direttamente in un file ASF, il grafico del filtro sarà simile al seguente, a seconda del tipo di dispositivo di acquisizione usato.

![grafico di acquisizione video di Windows Media](images/asf-webcam.png)

Per ulteriori informazioni sulla creazione di grafici di acquisizione video e audio, vedere gli argomenti seguenti:

-   [Acquisizione audio](audio-capture.md)
-   [Acquisizione video](video-capture.md)

Il writer ASF WM non verrà eseguito a meno che tutti i relativi pin non siano connessi. Se si configura il writer ASF WM con il profilo di sistema predefinito (scelta non consigliata) o qualsiasi profilo con flussi audio e video, verrà creato un pin di input per ogni flusso e ognuno di questi pin deve essere connesso. Se non si intende acquisire audio, ad esempio, assicurarsi di configurare il filtro con un profilo di solo video in modo che non venga creato alcun pin audio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



