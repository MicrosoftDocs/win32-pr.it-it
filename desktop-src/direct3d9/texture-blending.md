---
description: Direct3D può unire fino a otto trame sulle primitive in un singolo passaggio.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Blending di trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747618"
---
# <a name="texture-blending-direct3d-9"></a>Blending di trame (Direct3D 9)

Direct3D può unire fino a otto trame sulle primitive in un singolo passaggio. L'uso di più miscele di trame può aumentare in modo improprio la frequenza dei fotogrammi di un'applicazione Direct3D. Un'applicazione usa più miscele di trame per applicare trame, ombre, illuminazione speculare, illuminazione diffusa e altri effetti speciali in un singolo passaggio.

Per usare la combinazione di trame, l'applicazione deve prima verificare se l'hardware dell'utente lo supporta. Queste informazioni si trovano nel membro TextureCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Per informazioni dettagliate su come eseguire una query sull'hardware dell'utente per le funzionalità di combinazione di trame, vedere [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Fasi della trama e la combinazione di trama a cascata

Direct3D supporta la combinazione di più trame single-pass attraverso l'uso di fasi di trama. Una fase trama accetta due argomenti ed esegue un'operazione di fusione su di essi, passando il risultato per un'ulteriore elaborazione o per la rasterizzazione. È possibile visualizzare una fase di trama, come illustrato nel diagramma seguente.

![diagramma di una fase di trama](images/texstg.png)

Come illustrato nel diagramma precedente, le fasi della trama fondono due argomenti usando un operatore specificato. Le operazioni comuni includono la semplice modulazione o l'aggiunta di componenti di colore o alfa degli argomenti, ma sono supportate più di due dozzine di operazioni. Gli argomenti di una fase possono essere una trama associata, il colore iterato o alfa (iterato durante l'ombreggiatura Gouraud), il colore arbitrario e il valore alfa oppure il risultato della fase precedente della trama. Per altre informazioni, vedere [operazioni di combinazione di trame e argomenti (Direct3D 9)](texture-blending-operations-and-arguments.md).

> [!Note]  
> Direct3D distingue la fusione dei colori dalla fusione alfa. Le applicazioni impostano le operazioni di fusione e gli argomenti per colore e Alpha singolarmente e i risultati di tali impostazioni sono indipendenti l'uno dall'altro.

 

La combinazione di argomenti e operazioni utilizzate da più fasi di fusione definisce un linguaggio di fusione semplice basato sul flusso. I risultati di una fase scorrono verso il basso fino a un'altra fase, da quella fase alla successiva e così via. Il concetto di propagazione dei risultati dalla fase alla fase per la rasterizzazione in un poligono è spesso denominato Cascade blending Cascade. Il diagramma seguente illustra il modo in cui le singole fasi di trama costituiscono la fusione di trama a cascata.

![diagramma delle fasi della trama nella combinazione di trame a cascata](images/tcascade.png)

Ogni fase di un dispositivo ha un indice in base zero. Direct3D consente fino a otto fasi di fusione, sebbene sia sempre necessario controllare le funzionalità del dispositivo per determinare il numero di fasi supportate dall'hardware corrente. La prima fase di fusione si trova in corrispondenza dell'indice 0, il secondo è 1 e così via, fino all'indice 7. Il sistema combina le fasi nell'ordine di indice crescente.

Usare solo il numero di fasi necessarie; le fasi di fusione inutilizzate sono disabilitate per impostazione predefinita. Quindi, se l'applicazione usa solo le prime due fasi, è necessario impostare solo le operazioni e gli argomenti per la fase 0 e 1. Il sistema combina le due fasi e ignora le fasi disabilitate.

> [!Note]  
> Se l'applicazione varia il numero di fasi usato per diverse situazioni, ad esempio quattro fasi per alcuni oggetti e solo due per altri, non è necessario disabilitare in modo esplicito tutte le fasi usate in precedenza. Un'opzione consiste nel disabilitare l'operazione di colore per la prima fase inutilizzata, quindi non verranno applicate tutte le fasi con un indice superiore. Un'altra opzione consiste nel disabilitare completamente il mapping della trama impostando l'operazione di colore per la prima fase della trama (fase 0) su D3DTOP \_ Disable. Una terza opzione è quando una fase della trama ha D3DTSS \_ COLORARG1 uguale a D3DTA \_ trama e il puntatore di trama per la fase è **null**, questa fase e tutte le fasi dopo che non sono state elaborate.

 

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Operazioni di combinazione di trame e argomenti (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Assegnazione delle trame correnti (Direct3D 9)](assigning-the-current-textures.md)
-   [Creazione di fasi di fusione (Direct3D 9)](creating-blending-stages.md)
-   [Fusione di trame alfa (Direct3D 9)](alpha-texture-blending.md)
-   [Combinazione di trame multipass (Direct3D 9)](multipass-texture-blending.md)
-   [Mapping chiaro con trame (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
