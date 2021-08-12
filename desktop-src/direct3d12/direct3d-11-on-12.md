---
title: D3D11On12
description: D3D11On12 è un meccanismo tramite il quale gli sviluppatori possono usare interfacce e oggetti D3D11 per l'API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a67c7e0cd3592d35af80f280fc9f1893f4741fcadcc73afd3753880bccda3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530229"
---
# <a name="direct3d-11-on-12"></a>D3D11On12

D3D11On12 è un meccanismo tramite il quale gli sviluppatori possono usare interfacce e oggetti D3D11 per l'API D3D12. D3D11on12 consente ai componenti scritti con D3D11 (ad esempio, testo D2D e interfaccia utente) di funzionare insieme ai componenti scritti per l'API D3D12. D3D11on12 consente anche la portabilità incrementale di un'applicazione da D3D11 a D3D12, consentendo a parti dell'app di continuare a usare D3D11 come destinazione per semplicità, mentre altre hanno come destinazione D3D12 per le prestazioni, pur avendo sempre un rendering completo e corretto. D3D11On12 semplifica l'uso delle tecniche di interoperabilità per condividere le risorse e sincronizzare il lavoro tra le due API.

-   [Inizializzazione di D3D11On12](#initializing-d3d11on12)
-   [Utilizzo di esempio](#example-usage)
-   [Background](#background)
-   [Pulizia](#cleaning-up)
-   [Limitazioni](#limitations)
-   [API](#apis)
-   [Argomenti correlati](#related-topics)

## <a name="initializing-d3d11on12"></a>Inizializzazione di D3D11On12

Per iniziare a usare D3D11On12, il primo passaggio consiste nel creare un dispositivo D3D12 e una coda di comandi. Questi oggetti vengono forniti come input per il metodo di inizializzazione [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). È possibile pensare a questo metodo come alla creazione di un dispositivo D3D11 con il tipo di driver immaginario D3D DRIVER TYPE 11ON12, dove il driver D3D11 è responsabile della creazione di oggetti e dell'invio di elenchi di comandi \_ \_ \_ all'API D3D12.

Dopo aver creato un dispositivo D3D11 e un contesto immediato, è possibile disattivare il dispositivo per `QueryInterface` [**l'interfaccia ID3D11On12Device.**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) Questa è l'interfaccia principale usata per l'interoperabilità tra D3D11 e D3D12. Per fare in modo che il contesto di dispositivo D3D11 e gli elenchi di comandi D3D12 funzionino sulle stesse risorse, è necessario creare "risorse di cui è stato eseguito il wrapping" usando l'API [**CreateWrappedResource.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) Questo metodo "alza di livello" una risorsa D3D12 per essere comprensibile in D3D11. Una risorsa di cui è stato eseguito il wrapping inizia nello stato "acquisito", una proprietà che viene manipolata dai [**metodi AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) e [**ReleaseWrappedResources.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)

## <a name="example-usage"></a>Example Usage (Esempio di uso)

L'uso tipico di D3D11On12 è l'uso di D2D per eseguire il rendering di testo o immagini su un buffer nascosto D3D12. Vedere l'esempio D3D11On12 per il codice di esempio. Ecco una struttura approssimativa dei passaggi da eseguire a tale scopo:

-   Creare un dispositivo D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) e una catena di scambio D3D12 ([**CreateSwapChain con**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) come input).
-   Creare un dispositivo D3D11On12 usando il dispositivo D3D12 e la stessa coda di comandi dell'input.
-   Recuperare i buffer di back della catena di scambio e creare le risorse di cui è stato eseguito il wrapping D3D11 per ognuno di essi. Lo stato di input usato deve essere l'ultimo modo usato da D3D12 (ad esempio RENDER TARGET) e lo stato di output deve essere il modo in cui D3D12 lo userà al termine di \_ D3D11 (ad esempio PRESENT).
-   Inizializzare D2D e fornire le risorse di cui è stato eseguito il wrapping D3D11 a D2D per preparare il rendering.

Quindi, in ogni frame, eseguire le operazioni seguenti:

-   Eseguire il rendering nel buffer nascosto della catena di scambio corrente usando un elenco di comandi D3D12 ed eseguirlo.
-   Acquisire la risorsa di cui è stato eseguito il wrapping del buffer nascosto corrente ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Eseguire i comandi di rendering D2D.
-   Rilasciare la risorsa di cui è stato eseguito il wrapping ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Scaricare il contesto immediato D3D11.
-   Present ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Sfondo

D3D11On12 funziona in modo sistematico. Ogni chiamata API D3D11 passa attraverso la convalida di runtime tipica e passa al driver. A livello di driver, il driver speciale 11on12 registra lo stato e esegue operazioni di rendering in elenchi di comandi D3D12. Questi elenchi di comandi vengono inviati in base alle esigenze (ad esempio, una query o una risorsa potrebbe richiedere lo scaricamento dei comandi) o `GetData` come richiesto da `Map` Flush. La creazione di un oggetto D3D11 comporta in genere la creazione dell'oggetto D3D12 corrispondente. Alcune operazioni di rendering a funzione fissa in D3D11 come o non sono supportate `GenerateMips` `DrawAuto` in D3D12 e quindi D3D11On12 le emula usando shader e risorse aggiuntive.

Per l'interoperabilità, è importante comprendere in che modo D3D11On12 interagisce con gli oggetti D3D12 creati e forniti dall'app. Per garantire che il lavoro venga eseguita nell'ordine corretto, è necessario scaricare il contesto immediato D3D11 prima di poter inviare altro lavoro D3D12 a tale coda. È anche importante assicurarsi che la coda data a D3D11On12 sia sempre svuotabile. Ciò significa che tutte le attese nella coda devono essere soddisfatte, anche se il thread di rendering D3D11 si blocca per un periodo illimitato. È necessario non dipendere da quando D3D11On12 inserisce scaricamenti o attese, in quanto ciò potrebbe cambiare nelle versioni future. Inoltre, D3D11On12 tiene traccia e modifica gli stati delle risorse in modo proprio. L'unico modo per garantire la coerenza delle transizioni di stato è usare le API di acquisizione/rilascio per modificare il rilevamento dello stato in base alle esigenze dell'app.

## <a name="cleaning-up"></a>Pulizia

Per rilasciare una risorsa con wrapping D3D11On12, è necessario eseguire due operazioni nell'ordine seguente:

-   Tutti i riferimenti alla risorsa, incluse le visualizzazioni della risorsa, devono essere rilasciati.
-   Deve essere stata posticipata l'elaborazione della distruzione. Il modo più semplice per assicurarsi che ciò accada è richiamare l'API del contesto `Flush` immediato.

Al termine di entrambi questi passaggi, tutti i riferimenti eseuti dalla risorsa di cui è stato eseguito il wrapping devono essere rilasciati e la risorsa D3D12 diventa di proprietà esclusiva del componente D3D12. Tenere presente che D3D12 richiede ancora l'attesa del completamento della GPU prima di rilasciare completamente una risorsa, quindi assicurarsi di mantenere un riferimento alla risorsa prima di eseguire i due passaggi precedenti, a meno che non si sia già confermato che la GPU non sta più usando la risorsa.

Tutte le altre risorse o oggetti creati da D3D11On12 verranno puliti nel momento appropriato, quando la GPU ha terminato di usarli, usando il meccanismo di distruzione posticipata di D3D11. Tuttavia, se si tenta di rilasciare il dispositivo D3D11On12 mentre la GPU è ancora in esecuzione, la distruzione può bloccarsi fino al completamento della GPU.

## <a name="limitations"></a>Limitazioni

Il livello D3D11On12 implementa un subset molto grande dell'API D3D11, ma esistono alcune lacune note (oltre a bug nell'implementazione che possono causare rendering non corretto).

A Windows 10, versione 1809 (10.0; Build 17763), purché D3D11On12 sia in esecuzione in un driver che supporta il modello shader 6.0 o versione successiva, può eseguire shader che usano interfacce. Nelle versioni precedenti di Windows, la funzionalità delle interfacce shader non è implementata in D3D11On12 e il tentativo di usare la funzionalità causerà errori e messaggi di debug.

A Windows 10, versione 1803 (10.0; Build 17134), le catene di scambio sono supportate nei dispositivi D3D11On12. Nelle versioni precedenti di Windows, non lo sono.

D3D11On12 non è stato ottimizzato per le prestazioni. È probabile che si presenti un sovraccarico moderato della CPU rispetto a un driver D3D11 standard, un sovraccarico minimo della GPU e un sovraccarico di memoria significativo. Non è quindi consigliabile usare D3D11On12 per scene 3D complesse ed è invece consigliabile per scene semplici o rendering 2D.

## <a name="apis"></a>API

Le API che costituiscono il livello 11on12 sono descritte in [11on12 Reference (Informazioni di riferimento su 11on12).](direct3d-11on12-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura D2D con D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 