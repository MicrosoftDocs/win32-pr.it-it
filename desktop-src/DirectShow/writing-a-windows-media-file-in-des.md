---
description: Scrittura di un file di Windows Media in DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Scrittura di un file di Windows Media in DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320759"
---
# <a name="writing-a-windows-media-file-in-des"></a>Scrittura di un file di Windows Media in DES

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

In questa sezione viene descritto come scrivere un file Windows Media usando i [servizi di modifica DirectShow](directshow-editing-services.md) (des).

> [!IMPORTANT]
> Non usare il motore di rendering intelligente per scrivere file di Windows Media. Usare sempre il motore di rendering di base (CLSID \_ RenderEngine).

 

Per scrivere un file di Windows Media, procedere come segue:

1.  Chiamare il **sito Web** sul motore di rendering, con un puntatore al provider di chiavi.
2.  Compilare il front-end del grafo. Vedere [rendering di un progetto](rendering-a-project.md).
3.  Creare il filtro [WM ASF Writer](wm-asf-writer-filter.md) e aggiungerlo al grafico.
4.  Per impostare il nome del file, utilizzare l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) sul filtro WM ASF Writer.
5.  Configurare il writer ASF WM per l'utilizzo di un profilo Windows Media. Ogni profilo ha un numero predefinito di flussi. È necessario scegliere un profilo che corrisponda ai gruppi nel progetto.

    L'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contiene alcuni metodi diversi per l'impostazione del profilo. Ad esempio, il metodo **ConfigureFilterUsingProfileGuid** specifica un profilo di sistema come GUID. In alternativa, è possibile utilizzare i metodi Windows Media Format per ottenere un puntatore **IWMProfile** , quindi chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Per ulteriori informazioni, vedere [Configuring the ASF Writer](configuring-the-asf-writer.md).

6.  Connettere il front-end al writer ASF. Il front-end del grafico contiene un pin di output per ogni gruppo. Supponendo che sia stato specificato un profilo compatibile, il writer ASF deve avere un set di pin di input corrispondente. Connettere ogni pin di output al pin di input corrispondente. Il modo più semplice per eseguire questa operazione è usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . Per prima cosa, creare una nuova istanza del [Generatore di grafici di acquisizione](capture-graph-builder.md) e inizializzarla con un puntatore a gestione grafico dei filtri:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    Recuperare quindi il pin di output per ogni gruppo chiamando il metodo [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) . Chiamare **RenderStream** per connettere il PIN al writer ASF:

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Windows Media con i servizi di modifica DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



