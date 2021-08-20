---
title: Interoperabilità Direct3D 12
description: D3D12 può essere usato per scrivere applicazioni in componenti.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50bbf7af36c46513480b88a921ef79f8e534e7ffeca63fc4c8c34721b0578f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097753"
---
# <a name="direct3d-12-interop"></a>Interoperabilità Direct3D 12

D3D12 può essere usato per scrivere applicazioni in componenti.

-   [Panoramica dell'interoperabilità](#interop-overview)
-   [Motivi per l'uso dell'interoperabilità](#reasons-for-using-interop)
    -   [Condivisione di un elenco di comandi](#sharing-a-command-list)
    -   [Condivisione di una coda di comandi](#sharing-a-command-queue)
    -   [Condivisione delle primitive di sincronizzazione](#sharing-sync-primitives)
    -   [Condivisione di risorse](#sharing-resources)
    -   [Scelta di un modello di interoperabilità](#choosing-an-interop-model)
-   [API di interoperabilità](#interop-apis)
-   [Argomenti correlati](#related-topics)

## <a name="interop-overview"></a>Panoramica dell'interoperabilità

D3D12 può essere molto potente e consente alle applicazioni di scrivere codice grafico con efficienza simile a quella della console, ma non tutte le applicazioni devono inventare la ruota e scrivere l'intero motore di rendering da zero. In alcuni casi, un altro componente o libreria lo ha già fatto meglio o, in altri casi, le prestazioni di una parte di codice non sono critiche quanto la correttezza e la leggibilità.

Questa sezione illustra le tecniche di interoperabilità seguenti:

-   D3D12 e D3D12 nello stesso dispositivo
-   D3D12 e D3D12 in dispositivi diversi
-   D3D12 e qualsiasi combinazione di D3D11, D3D10 o D2D nello stesso dispositivo
-   D3D12 e qualsiasi combinazione di D3D11, D3D10 o D2D in dispositivi diversi
-   D3D12 e GDI o D3D12 e D3D11 e GDI

## <a name="reasons-for-using-interop"></a>Motivi per l'uso dell'interoperabilità

Esistono diversi motivi per cui un'applicazione vuole l'interoperabilità D3D12 con altre API. Di seguito alcuni esempi:

-   Portabilità incrementale: si vuole eseguire il porting di un'intera applicazione da D3D10 o D3D11 a D3D12, mantenendola funzionante nelle fasi intermedie del processo di portabilità (per abilitare il test e il debug).
-   Codice Black Box: se si vuole lasciare una particolare parte di un'applicazione così com'è durante la portabilità del resto del codice. Ad esempio, potrebbe non essere necessario convertire gli elementi dell'interfaccia utente di un gioco.
-   Componenti non modificabili: è necessario usare componenti che non sono di proprietà dell'applicazione, che non vengono scritti nella destinazione D3D12.
-   Un nuovo componente: non si vuole convertire l'intera applicazione, ma si vuole usare un nuovo componente scritto con D3D12.

Esistono quattro tecniche principali per l'interoperabilità in D3D12:

-   Un'app può scegliere di fornire un elenco di comandi aperto a un componente, che registra alcuni comandi di rendering aggiuntivi in una destinazione di rendering già associata. Ciò equivale a fornire un contesto di dispositivo preparato a un altro componente in D3D11 ed è ideale per operazioni come l'aggiunta di interfaccia utente/testo a un buffer nascosto già associato.
-   Un'app può scegliere di fornire una coda di comandi a un componente, insieme a una risorsa di destinazione desiderata. Equivale a usare le API [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) o [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) in D3D11 per fornire un contesto di dispositivo pulito a un altro componente. Ecco come funzionano i componenti come D2D.
-   Un componente può scegliere un modello in cui produce un elenco di comandi, potenzialmente in parallelo, che l'app è responsabile dell'invio in un secondo momento. È necessario fornire almeno una risorsa oltre i limiti dei componenti. Questa stessa tecnica è disponibile in D3D11 usando contesti posticied, anche se le prestazioni in D3D12 sono più desiderabili.
-   Ogni componente ha le proprie code e/o dispositivi e l'app e i componenti devono condividere le risorse e le informazioni di sincronizzazione tra i limiti dei componenti. È simile al legacy e al più `ISurfaceQueue` moderno [**IDXGIKeyedMutex.**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)

Le differenze tra questi scenari sono esattamente quelle condivise tra i limiti dei componenti. Si presuppone che il dispositivo sia condiviso, ma poiché è fondamentalmente senza stato, non è realmente rilevante. Gli oggetti chiave sono l'elenco dei comandi, la coda dei comandi, gli oggetti di sincronizzazione e le risorse. Ognuno di questi elementi presenta complicazioni durante la condivisione.

### <a name="sharing-a-command-list"></a>Condivisione di un elenco di comandi

Il metodo di interoperabilità più semplice richiede la condivisione solo di un elenco di comandi con una parte del motore. Al termine delle operazioni di rendering, la proprietà dell'elenco di comandi torna al chiamante. La proprietà dell'elenco di comandi può essere tracciata tramite lo stack. Poiché gli elenchi di comandi sono a thread singolo, non è possibile per un'app eseguire un'operazione univoca o innovative usando questa tecnica.

### <a name="sharing-a-command-queue"></a>Condivisione di una coda di comandi

Probabilmente la tecnica più comune per più componenti che condividono un dispositivo nello stesso processo.

Quando la coda di comandi è l'unità di condivisione, deve essere presente una chiamata al componente per insoddirlo che tutti gli elenchi di comandi in sospeso devono essere inviati immediatamente alla coda dei comandi (ed eventuali code di comandi interne devono essere sincronizzate). Equivale [**all'API**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) Flush D3D11 ed è l'unico modo in cui l'applicazione può inviare i propri elenchi di comandi o primitive di sincronizzazione.

### <a name="sharing-sync-primitives"></a>Condivisione delle primitive di sincronizzazione

Il modello previsto per un componente che opera sui propri dispositivi e/o sulle code di comandi prevede l'accettazione di un handle [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) o condiviso e della coppia UINT64 all'inizio del lavoro, che attenderà, e quindi di un secondo handle CONDIVISO o ID3D12Fence e uiNT64 che segnalerà al termine di tutte le operazioni. Questo modello corrisponde all'implementazione corrente di [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) e della progettazione della sincronizzazione del modello flip DWM/DXGI.

### <a name="sharing-resources"></a>Condivisione di risorse

Di gran lunga la parte più complessa della scrittura di un'app D3D12 che sfrutta più componenti è come gestire le risorse condivise tra i limiti dei componenti. Ciò è dovuto principalmente al concetto di stati delle risorse. Anche se alcuni aspetti della progettazione dello stato delle risorse sono destinati a gestire la sincronizzazione all'interno dell'elenco dei comandi, altri influiscono tra gli elenchi di comandi, influiscono sul layout delle risorse e su set validi di operazioni o sulle caratteristiche delle prestazioni di accesso ai dati delle risorse.

Esistono due modelli di gestione di questa complicazione, entrambi che implicano essenzialmente un contratto tra componenti.

-   Il contratto può essere definito dallo sviluppatore del componente e documentato. Può essere semplice quanto "la risorsa deve essere nello stato predefinito all'avvio del lavoro e verrà impostata di nuovo sullo stato predefinito al termine del lavoro" o potrebbe avere regole più complesse per consentire operazioni come la condivisione di un buffer di profondità senza forzare la risoluzione della profondità intermedia.
-   Il contratto può essere definito dall'applicazione in fase di esecuzione, nel momento in cui la risorsa è condivisa tra i limiti del componente. È costituita dalle stesse due informazioni: lo stato in cui si presenterà la risorsa quando il componente inizia a usarla e lo stato in cui il componente deve lasciarla al termine dell'operazione.

### <a name="choosing-an-interop-model"></a>Scelta di un modello di interoperabilità

Per la maggior parte delle applicazioni D3D12, la condivisione di una coda di comandi è probabilmente il modello ideale. Consente la proprietà completa della creazione e dell'invio del lavoro, senza il sovraccarico di memoria aggiuntivo dovuto alla presenza di code ridondanti e senza l'impatto sulle prestazioni della gestione delle primitive di sincronizzazione GPU.

La condivisione delle primitive di sincronizzazione è necessaria quando i componenti devono gestire proprietà della coda diverse, ad esempio il tipo o la priorità, o quando la condivisione deve estendersi oltre i limiti del processo.

La condivisione o la produzione di elenchi di comandi non sono ampiamente usate esternamente da componenti di terze parti, ma possono essere ampiamente usate nei componenti interni a un motore di gioco.

## <a name="interop-apis"></a>API di interoperabilità

[L'argomento Direct3D 11 on 12 (Direct3D 11 su 12)](./direct3d-11-on-12.md) illustra l'uso di gran parte della superficie dell'API correlata ai tipi di interoperatività descritti in questo argomento.

Vedere anche [il metodo ID3D12Device::CreateSharedHandle,](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) che è possibile usare per condividere le superfici tra Windows API grafiche.

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni su Direct3D 12](directx-12-getting-started.md)
* [Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
* [D3D11On12](./direct3d-11-on-12.md)