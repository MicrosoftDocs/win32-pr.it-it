---
description: Creazione di un grafico di acquisizione audio con anteprima
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Creazione di un grafico di acquisizione audio con anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965856"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>Creazione di un grafico di acquisizione audio con anteprima

Il grafico di filtro descritto in [creazione di un grafico di acquisizione audio](creating-an-audio-capture-graph.md) esegue solo l'acquisizione, senza anteprima. Per visualizzare in anteprima e acquisire allo stesso tempo, è necessario che il grafico di filtro usi il [filtro del Pin Tee infinito](infinite-pin-tee-filter.md). Questo filtro ha un pin di input e crea tutti i pin di output in base alle esigenze. (Inizia con un pin di output. Ogni volta che si connette un pin di output, ne crea un altro. Il filtro del Pin Tee infinito recapita ogni campione che riceve, senza modifiche, attraverso tutti i relativi pin di output.

Connettere il filtro di acquisizione audio al Pin Tee infinito e connettere il pin infinito al multiplexer e al [filtro di renderer DirectSound](directsound-renderer-filter.md). Connettere il multiplexer al writer di file, come prima. Il diagramma seguente illustra il grafico filtro risultante per un file AVI.

![grafico di acquisizione audio con anteprima](images/audio-capture-graph.png)

Poiché il renderer DirectSound è il renderer audio predefinito, è possibile chiamare semplicemente il metodo [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) sul pin di output del Pin Tee infinito. Il gestore del grafico del filtro utilizza la [connessione intelligente](intelligent-connect.md) per creare il renderer, aggiungerlo al grafico di filtro e connettere i pin.

> [!Note]  
> Se si acquisisce audio da un microfono e lo si visualizza in anteprima da un altoparlante nello stesso computer, è possibile creare commenti e suggerimenti audio.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



