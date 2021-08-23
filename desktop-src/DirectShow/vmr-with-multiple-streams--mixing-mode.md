---
description: VMR con più Flussi (modalità di combinazione)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR con più Flussi (modalità di combinazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f958d8c95372325229dffc1cc37aff579213c48940f93ad090d0fbd9359b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290781"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR con più Flussi (modalità di combinazione)

La macchina virtuale può eseguire il rendering di più flussi di input. In questa configurazione, denominata modalità di combinazione, la macchina virtuale carica il mixer e il compositor per eseguire la combinazione e la fusione prima del rendering. La modalità di combinazione può essere usata mentre la macchina virtuale è in modalità finestra o senza finestra.

La modalità di combinazione richiede che il driver di grafica supporti i flag di funzionalità \_ DDCAPS BLTFOURCC e DDCAPS BLTSTRETCH (rispettivamente conversione dello spazio colore e \_ blttting di estensione). Quasi tutti i nuovi driver di grafica hanno queste funzionalità. Inoltre, il driver deve supportare la creazione di destinazioni di rendering Direct3D per la profondità in pixel di visualizzazione corrente. Alcuni dispositivi non supportano le operazioni Direct3D quando lo schermo è impostato su 24 bit per pixel. Per altre informazioni, vedere la documentazione di DirectX Graphics SDK.

> [!Note]  
> Quando la macchina virtuale combina più flussi video, il grafico dei filtri non esegue correttamente la ricerca. Se è necessario cercare più flussi video, è necessario creare grafici di filtro separati che condividono lo stesso oggetto allocatore-presentatore personalizzato.

 

**Configurazione di VMR-7 per più Flussi**

Per eseguire il rendering di più flussi di input con VMR-7, seguire questa procedura:

1.  Prima di connettere uno dei pin di input della macchina virtuale, chiamare il metodo [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) con il numero di flussi. In questo modo la macchina virtuale carica il mixer e il compositor e crea il numero specificato di pin di input.
2.  Chiamare [**IVMRFilterConfig::SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) per specificare diverse preferenze di rendering.
3.  Connessione i pin ai filtri upstream. Il modo più semplice per eseguire questa operazione è chiamare [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) per ogni flusso di input. Se il pin di output nel filtro upstream (in genere un decodificatore) e il pin di input nella macchina virtuale non sono in grado di concordare una connessione, verrà creata una nuova istanza del vmr con le impostazioni predefinite. Verrà visualizzata una nuova finestra con "ActiveMovie" nella barra del titolo. Per evitare che ciò accada, l'applicazione deve sempre verificare che venga usata l'istanza corretta della macchina virtuale chiamando un metodo come [**IPin::ConnectedTo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) Un'altra opzione è aggiungere il filtro di origine e quindi connettere i segnaposto **usando IGraphBuilder::Connessione**.
4.  Usare [**l'interfaccia IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) nella macchina virtuale per controllare i parametri per ogni flusso, ad esempio il valore alfa, l'ordinamento Z e il rettangolo di output.
5.  Eseguire il grafico del filtro.

**Configurazione di VMR-9 per più Flussi**

Per impostazione predefinita, VMR-9 crea quattro pin di input. Se si vogliono combinare più di quattro flussi video, chiamare [**IVMRFilterConfig9::SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) prima di connettere eventuali pin di input. Usare [**l'interfaccia IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) per impostare i parametri del flusso, ad esempio alfa, ordine Z e posizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



