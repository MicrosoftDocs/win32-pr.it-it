---
title: D3D11On12
description: D3D11On12 è un meccanismo mediante il quale gli sviluppatori possono usare le interfacce e gli oggetti di D3D11 per guidare l'API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548787"
---
# <a name="direct3d-11-on-12"></a>D3D11On12

D3D11On12 è un meccanismo mediante il quale gli sviluppatori possono usare le interfacce e gli oggetti di D3D11 per guidare l'API D3D12. D3D11on12 consente ai componenti scritti con D3D11, ad esempio D2D testo e interfaccia utente, di interagire con i componenti scritti per l'API D3D12. D3D11on12 consente anche il porting incrementale di un'applicazione da D3D11 a D3D12, consentendo a parti dell'app di continuare a usare D3D11 per semplicità, mentre altre sono destinate a D3D12 per le prestazioni, pur avendo sempre il rendering completo e corretto. D3D11On12 rende più semplice l'uso di tecniche di interoperabilità per condividere le risorse e sincronizzare il lavoro tra le due API.

-   [Inizializzazione di D3D11On12](#initializing-d3d11on12)
-   [Esempio di utilizzo](#example-usage)
-   [Background](#background)
-   [Pulizia](#cleaning-up)
-   [Limitazioni](#limitations)
-   [API](#apis)
-   [Argomenti correlati](#related-topics)

## <a name="initializing-d3d11on12"></a>Inizializzazione di D3D11On12

Per iniziare a usare D3D11On12, il primo passaggio consiste nel creare un dispositivo D3D12 e una coda di comandi. Questi oggetti vengono forniti come input per il metodo di inizializzazione [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). È possibile considerare questo metodo come la creazione di un dispositivo D3D11 con il tipo di driver D3D tipo di driver D3D \_ \_ \_ 11ON12, in cui il driver d3d11 è responsabile della creazione di oggetti e dell'invio di elenchi di comandi all'API D3D12.

Quando si dispone di un dispositivo D3D11 e di un contesto immediato, è possibile `QueryInterface` disattivare il dispositivo per l'interfaccia [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) . Si tratta dell'interfaccia primaria utilizzata per l'interoperabilità tra D3D11 e D3D12. Per fare in modo che il contesto di dispositivo D3D11 e gli elenchi di comandi D3D12 funzionino sulle stesse risorse, è necessario creare "risorse incapsulate" tramite l'API [**CreateWrappedResource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) . Questo metodo "promuove" una risorsa D3D12 che deve essere comprensibile in D3D11. Una risorsa di cui è stato eseguito il wrapper inizia nello stato "acquisito", una proprietà che viene modificata dai metodi [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) e [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) .

## <a name="example-usage"></a>Example Usage (Esempio di uso)

L'utilizzo tipico di D3D11On12 è l'uso di D2D per il rendering di testo o immagini su un buffer nascosto di D3D12. Per un esempio di codice, vedere l'esempio D3D11On12. Di seguito è riportato un abbozzo dei passaggi da eseguire per eseguire questa operazione:

-   Creare un dispositivo D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) e una catena di scambio D3D12 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) con un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) come input).
-   Creare un dispositivo D3D11On12 usando il dispositivo D3D12 e la stessa coda dei comandi come input.
-   Recuperare i buffer indietro della catena di scambio e creare risorse di cui è stato eseguito il wrapper D3D11 per ognuno di essi. Lo stato di input usato deve essere l'ultimo modo in cui D3D12 lo usava, ad esempio la destinazione di rendering \_ , e lo stato di output dovrebbe essere il modo in cui D3D12 lo userà al termine di d3d11 (ad esempio, presente).
-   Inizializzare D2D e fornire le risorse D3D11 incapsulate a D2D per prepararsi al rendering.

Quindi, in ogni frame eseguire le operazioni seguenti:

-   Eseguire il rendering nel buffer back chain di scambio corrente usando un elenco di comandi D3D12 ed eseguirlo.
-   Acquisisce la risorsa di cui è stato eseguito il wrapper ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Rilascia i comandi di rendering D2D.
-   Rilasciare la risorsa di cui è stato eseguito il wrapper ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Svuotare il contesto D3D11 immediato.
-   Presente ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Sfondo

D3D11On12 funziona sistematicamente. Ogni chiamata all'API D3D11 passa attraverso la convalida del runtime tipica e ne esegue il passaggio al driver. A livello di driver, il driver 11on12 speciale registra lo stato e rilascia le operazioni di rendering agli elenchi di comandi D3D12. Questi elenchi di comandi vengono inviati in base alle esigenze (ad esempio, una query `GetData` o una risorsa `Map` potrebbe richiedere lo scaricamento dei comandi) o come richiesto dallo svuotamento. La creazione di un oggetto D3D11 in genere comporta la creazione dell'oggetto D3D12 corrispondente. Alcune operazioni di rendering di funzioni fisse in D3D11 `GenerateMips` , ad esempio o `DrawAuto` , non sono supportate in D3D12, quindi D3D11On12 le emula usando shader e risorse aggiuntive.

Per l'interoperabilità, è importante comprendere il modo in cui D3D11On12 interagisce con gli oggetti D3D12 creati e forniti dall'app. Per assicurarsi che il lavoro avvenga nell'ordine corretto, è necessario scaricare il contesto immediato di D3D11 prima di poter inviare ulteriori attività D3D12 a tale coda. È inoltre importante assicurarsi che la coda assegnata a D3D11On12 debba essere scaricabile sempre. Ciò significa che qualsiasi attesa nella coda deve essere soddisfatta, anche se il thread di rendering D3D11 si blocca a tempo indefinito. Prestare attenzione a non dipendere dal momento in cui D3D11On12 inserimenti cancellati o attese, perché questo potrebbe cambiare nelle versioni future. Inoltre, D3D11On12 tiene traccia e manipola gli Stati delle risorse autonomamente. L'unico modo per garantire la coerenza delle transizioni di stato consiste nell'usare le API di acquisizione/rilascio per modificare il rilevamento dello stato in modo che corrisponda alle esigenze dell'app.

## <a name="cleaning-up"></a>Pulizia

Per rilasciare una risorsa D3D11On12 di cui è stato eseguito il wrapper, è necessario eseguire due operazioni nell'ordine seguente:

-   È necessario rilasciare tutti i riferimenti alla risorsa, incluse tutte le visualizzazioni della risorsa.
-   È necessario eseguire l'elaborazione della distruzione posticipata. Il modo più semplice per verificare questo problema consiste nel richiamare l'API del contesto immediato `Flush` .

Una volta completati entrambi questi passaggi, verranno rilasciati tutti i riferimenti eseguiti dalla risorsa di cui è stato eseguito il wrapper e la risorsa D3D12 diventerà esclusivamente il componente D3D12. Tenere presente che D3D12 richiede ancora l'attesa del completamento della GPU prima di rilasciare completamente una risorsa. Assicurarsi quindi di conservare un riferimento sulla risorsa prima di eseguire i due passaggi precedenti, a meno che non sia già stato confermato che la GPU non sta più usando la risorsa.

Tutte le altre risorse o oggetti creati da D3D11On12 verranno puliti al momento opportuno, al termine dell'uso della GPU, usando il meccanismo di distruzione posticipato di D3D11's. Tuttavia, se si tenta di rilasciare il dispositivo D3D11On12 mentre la GPU è ancora in esecuzione, è possibile che la distruzione si blocchi fino al completamento della GPU.

## <a name="limitations"></a>Limitazioni

Il livello D3D11On12 implementa un subset molto grande dell'API D3D11, ma esistono alcuni gap noti, oltre ai bug nell'implementazione che possono causare il rendering errato.

A partire da Windows 10, versione 1809 (10,0; Build 17763), a condizione che D3D11On12 sia in esecuzione su un driver che supporta Shader Model 6,0 o versione successiva, può eseguire shader che usano le interfacce. Nelle versioni precedenti di Windows, la funzionalità delle interfacce dello shader non è implementata in D3D11On12 e il tentativo di utilizzare la funzionalità provocherà errori e messaggi di debug.

A partire da Windows 10, versione 1803 (10,0; Build 17134), le catene di scambio sono supportate nei dispositivi D3D11On12. Nelle versioni precedenti di Windows non lo sono.

D3D11On12 non è stato ottimizzato per le prestazioni. È probabile che si verifichi un sovraccarico della CPU moderato rispetto a un driver D3D11 standard, un sovraccarico minimo della GPU ed è noto un sovraccarico significativo della memoria. Non è quindi consigliabile usare D3D11On12 per scene 3D complesse ed è invece consigliabile per le scene semplici o per il rendering 2D.

## <a name="apis"></a>API

Le API che compongono il livello 11on12 sono descritte in [riferimento a 11on12](direct3d-11on12-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D2D con la procedura dettagliata D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 