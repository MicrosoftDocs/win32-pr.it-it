---
title: Introduzione al multithreading in Direct3D 11
description: Il multithreading è progettato per migliorare le prestazioni eseguendo il lavoro utilizzando uno o più thread contemporaneamente.
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337559"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Introduzione al multithreading in Direct3D 11

Il multithreading è progettato per migliorare le prestazioni eseguendo il lavoro utilizzando uno o più thread contemporaneamente.

In passato, questa operazione è stata spesso eseguita generando un singolo thread principale per il rendering e uno o più thread per eseguire operazioni di preparazione, ad esempio la creazione, il caricamento, l'elaborazione e così via degli oggetti. Con la sincronizzazione incorporata in Direct3D 11, tuttavia, l'obiettivo del multithreading consiste nell'utilizzare ogni ciclo della CPU e della GPU senza che un processore attenda un altro processore (in particolare, non facendo attendere la GPU perché influisca direttamente sulla frequenza dei fotogrammi). In questo modo, è possibile generare la maggior parte del lavoro mantenendo la frequenza dei fotogrammi migliore. Il concetto di un singolo frame per il rendering non è più necessario perché l'API implementa la sincronizzazione.

Il multithreading richiede una qualche forma di sincronizzazione. Se, ad esempio, più thread eseguiti in un'applicazione devono accedere a un contesto di dispositivo singolo ([**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)), l'applicazione deve utilizzare un meccanismo di sincronizzazione, ad esempio sezioni critiche, per sincronizzare l'accesso a tale contesto di dispositivo. Ciò è dovuto al fatto che l'elaborazione dei comandi di rendering (in genere eseguita sulla GPU) e la generazione dei comandi di rendering (in genere eseguiti sulla CPU tramite la creazione di oggetti, il caricamento dei dati, la modifica dello stato e l'elaborazione dei dati) spesso utilizzano le stesse risorse (trame, shader, stato della pipeline e così via). Per organizzare il lavoro tra più thread, è necessario eseguire la sincronizzazione per impedire che un thread modifichi o legga i dati modificati da un altro thread.

Mentre l'uso di un contesto di dispositivo ([**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) non è thread-safe, l'uso di un dispositivo Direct3D 11 ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) è thread-safe. Poiché ogni **sul ID3D11DeviceContext** è a thread singolo, solo un thread può chiamare un **sul ID3D11DeviceContext** alla volta. Se più thread devono accedere a un singolo **sul ID3D11DeviceContext**, devono usare un meccanismo di sincronizzazione, ad esempio sezioni critiche, per sincronizzare l'accesso a tale **sul ID3D11DeviceContext**. Tuttavia, non è necessario che più thread usino sezioni critiche o primitive di sincronizzazione per accedere a un singolo **ID3D11Device**. Se quindi un'applicazione usa **ID3D11Device** per creare oggetti risorsa, non è necessario che l'applicazione usi la sincronizzazione per creare più oggetti risorsa nello stesso momento.

Il supporto per il multithreading divide l'API in due aree funzionali distinte:

-   [Creazione di oggetti con multithreading](overviews-direct3d-11-render-multi-thread-create.md)
-   [Rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md)

Le prestazioni del multithreading dipendono dal supporto del driver. [Procedura: cercare supporto driver](overviews-direct3d-11-render-multi-thread-support.md) fornisce altre informazioni sull'esecuzione di query sul driver e sul significato dei risultati.

Direct3D 11 è stato progettato da zero per supportare il multithreading. Direct3D 10 implementa un supporto limitato per il multithreading utilizzando il [livello thread-safe](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers). In questa pagina sono elencate le differenze di comportamento tra le due versioni di DirectX: le [differenze di threading tra le versioni di Direct3D](overviews-direct3d-11-render-multi-thread-differences.md).

## <a name="multithreading-and-dxgi"></a>Multithreading e DXGI

Un solo thread alla volta deve usare il contesto immediato. Tuttavia, l'applicazione deve usare anche lo stesso thread per le operazioni di Microsoft DirectX Graphics Infrastructure (DXGI), soprattutto quando l'applicazione effettua chiamate al metodo [**IDXGISwapChain::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) reinviate.

> [!Note]  
> Non è possibile usare contemporaneamente un contesto immediato con la maggior parte delle funzioni dell'interfaccia DXGI. Per gli SDK DirectX 2009 e versioni successive, le uniche funzioni DXGI sicure sono [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

 

Per altre informazioni sull'uso di DXGI con più thread, vedere [considerazioni su multithread](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 