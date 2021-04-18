---
description: VMR con più flussi (modalità di combinazione)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR con più flussi (modalità di combinazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314369"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR con più flussi (modalità di combinazione)

VMR è in grado di eseguire il rendering di più flussi di input. In questa configurazione, chiamata modalità di combinazione, VMR carica il mixer e il compositor per eseguire la combinazione e la fusione prima del rendering. La modalità di combinazione può essere usata quando il VMR è in modalità finestra o in modalità senza finestra.

Per la modalità di combinazione è necessario che il driver di grafica supporti i \_ flag di funzionalità DDCAPS BLTFOURCC e DDCAPS \_ BLTSTRETCH (rispettivamente conversione dello spazio dei colori e stretch blitting). Quasi tutti i nuovi driver grafici hanno le stesse funzionalità. Inoltre, il driver deve supportare la creazione di destinazioni di rendering Direct3D per la profondità dei pixel di visualizzazione corrente. Alcuni dispositivi non supportano le operazioni Direct3D quando la visualizzazione è impostata su 24 bit per pixel. Per ulteriori informazioni, vedere la documentazione di DirectX Graphics SDK.

> [!Note]  
> Quando VMR combina più flussi video, il grafico del filtro non viene cercato correttamente. Se è necessario cercare più flussi video, è necessario creare grafici di filtro distinti che condividono lo stesso oggetto allocatore-Presenter personalizzato.

 

**Configurazione di VMR-7 per più flussi**

Per eseguire il rendering di più flussi di input con VMR-7, eseguire le operazioni seguenti:

1.  Prima di connettere i pin di input di VMR, chiamare il metodo [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) con il numero di flussi. In questo modo, il VMR caricherà il mixer e il compositor e creerà il numero specificato di pin di input.
2.  Chiamare [**IVMRFilterConfig:: SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) per specificare diverse preferenze di rendering.
3.  Connettere i pin ai filtri upstream. Il modo più semplice per eseguire questa operazione è chiamare [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) per ogni flusso di input. Se il pin di output sul filtro upstream (in genere un decodificatore) e il pin di input in VMR non sono in grado di accettare una connessione, verrà creata una nuova istanza di VMR con le impostazioni predefinite. Verrà generata una nuova finestra con "ActiveMovie" nella barra del titolo. Per evitare che ciò accada, l'applicazione deve sempre verificare che venga usata l'istanza corretta di VMR chiamando un metodo come [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto). Un'altra opzione consiste nell'aggiungere il filtro di origine e quindi connettere i pin usando **IGraphBuilder:: Connect**.
4.  Usare l'interfaccia [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) in VMR per controllare i parametri per ogni flusso, ad esempio il valore alfa, l'ordinamento Z e il rettangolo di output.
5.  Eseguire il grafico dei filtri.

**Configurazione di VMR-9 per più flussi**

Per impostazione predefinita, VMR-9 crea quattro pin di input. Se si vogliono combinare più di quattro flussi video, chiamare [**IVMRFilterConfig9:: SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) prima di connettere i pin di input. Usare l'interfaccia [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) per impostare i parametri del flusso, ad esempio Alpha, Z-order e position.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



