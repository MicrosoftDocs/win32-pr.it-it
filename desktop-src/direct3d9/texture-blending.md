---
description: Direct3D può unire fino a otto trame in primitive in un singolo passaggio.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Fusione tra trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688be4c80fb87d0d96f8f930ed85c9cc934fc4392151196ec0c510a4cbe482bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291607"
---
# <a name="texture-blending-direct3d-9"></a>Fusione tra trame (Direct3D 9)

Direct3D può unire fino a otto trame in primitive in un singolo passaggio. L'uso della fusione di più trame può aumentare notevolmente la frequenza dei fotogrammi di un'applicazione Direct3D. Un'applicazione usa più combinazioni di trame per applicare trame, ombreggiature, illuminazione speculare, illuminazione diffusa e altri effetti speciali in un singolo passaggio.

Per usare la fusione di trame, l'applicazione deve prima verificare se l'hardware dell'utente lo supporta. Queste informazioni sono disponibili nel membro TextureCaps della [**struttura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Per informazioni dettagliate su come eseguire query sull'hardware dell'utente per le funzionalità di fusione delle trame, vedere [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Fasi di trama e cascata di fusione tra trame

Direct3D supporta la fusione di più trame a passaggio singolo tramite l'uso di fasi di trama. Una fase di trama accetta due argomenti ed esegue un'operazione di fusione su di essi, passando il risultato per un'ulteriore elaborazione o per la rasterizzazione. È possibile visualizzare una fase della trama, come illustrato nel diagramma seguente.

![diagramma di una fase di trama](images/texstg.png)

Come illustrato nel diagramma precedente, le fasi di trama combinano due argomenti usando un operatore specificato. Le operazioni comuni includono la semplice modulazione o l'aggiunta dei componenti colore o alfa degli argomenti, ma sono supportate più di due decine di operazioni. Gli argomenti per una fase possono essere una trama associata, il colore iterato o alfa (iterato durante l'ombreggiatura Gouraud), il colore arbitrario e il valore alfa o il risultato della fase precedente della trama. Per altre informazioni, vedere Operazioni e argomenti di [fusione tra trame (Direct3D 9).](texture-blending-operations-and-arguments.md)

> [!Note]  
> Direct3D distingue la fusione dei colori dalla fusione alfa. Le applicazioni impostano le operazioni di fusione e gli argomenti per colore e alfa singolarmente e i risultati di tali impostazioni sono indipendenti l'uno dall'altro.

 

La combinazione di argomenti e operazioni usate da più fasi di fusione definisce un linguaggio di fusione semplice basato sul flusso. I risultati di una fase vengono visualizzati in un'altra fase, da tale fase a quella successiva e così via. Il concetto di risultati che scorrono da una fase all'altro per essere rasterizzati in un poligono è spesso chiamato cascata di fusione della trama. Il diagramma seguente illustra come le singole fasi della trama costituiscono la cascata di fusione tra trame.

![Diagramma delle fasi della trama nella cascata di fusione tra trame](images/tcascade.png)

Ogni fase di un dispositivo ha un indice in base zero. Direct3D consente fino a otto fasi di fusione, anche se è necessario controllare sempre le funzionalità del dispositivo per determinare il numero di fasi supportate dall'hardware corrente. La prima fase di fusione è in corrispondenza dell'indice 0, la seconda a 1 e così via, fino all'indice 7. Il sistema combina le fasi in ordine di indice crescente.

Usare solo il numero di fasi necessarie. Le fasi di fusione non utilizzate sono disabilitate per impostazione predefinita. Pertanto, se l'applicazione usa solo le prime due fasi, è necessario impostare solo operazioni e argomenti per le fasi 0 e 1. Il sistema combina le due fasi e ignora le fasi disabilitate.

> [!Note]  
> Se l'applicazione varia il numero di fasi usate per situazioni diverse, ad esempio quattro fasi per alcuni oggetti e solo due per altre, non è necessario disabilitare in modo esplicito tutte le fasi usate in precedenza. Un'opzione è disabilitare l'operazione di colore per la prima fase inutilizzata, quindi tutte le fasi con un indice superiore non verranno applicate. Un'altra opzione consiste nel disabilitare completamente il mapping delle trame impostando l'operazione di colore per la prima fase della trama (fase 0) su D3DTOP \_ DISABLE. Una terza opzione è quando una fase di trama ha D3DTSS COLORARG1 uguale a D3DTA TEXTURE e il puntatore di trama per la fase \_ \_ è **NULL,** questa fase e tutte le fasi dopo non vengono elaborate.

 

Altre informazioni sono contenute negli argomenti seguenti.

-   [Operazioni e argomenti di fusione tra trame (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Assegnazione delle trame correnti (Direct3D 9)](assigning-the-current-textures.md)
-   [Creazione di fasi di fusione (Direct3D 9)](creating-blending-stages.md)
-   [Fusione trame alfa (Direct3D 9)](alpha-texture-blending.md)
-   [Fusione di trame multipass (Direct3D 9)](multipass-texture-blending.md)
-   [Mapping di luce con trame (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
