---
title: Interoperabilità di Direct3D 12
description: D3D12 può essere usato per scrivere applicazioni con componenti.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548892"
---
# <a name="direct3d-12-interop"></a>Interoperabilità di Direct3D 12

D3D12 può essere usato per scrivere applicazioni con componenti.

-   [Panoramica dell'interoperabilità](#interop-overview)
-   [Motivi per l'utilizzo dell'interoperabilità](#reasons-for-using-interop)
    -   [Condivisione di un elenco di comandi](#sharing-a-command-list)
    -   [Condivisione di una coda di comandi](#sharing-a-command-queue)
    -   [Condivisione delle primitive di sincronizzazione](#sharing-sync-primitives)
    -   [Condivisione di risorse](#sharing-resources)
    -   [Scelta di un modello di interoperabilità](#choosing-an-interop-model)
-   [API di interoperabilità](#interop-apis)
-   [Argomenti correlati](#related-topics)

## <a name="interop-overview"></a>Panoramica dell'interoperabilità

D3D12 può essere molto potente e consentire alle applicazioni di scrivere codice grafico con efficienza simile a console, ma non tutte le applicazioni devono riinventare la ruota e scrivere completamente il motore di rendering da zero. In alcuni casi, un altro componente o libreria ha già eseguito una soluzione migliore o, in altri casi, le prestazioni di una parte di codice non sono cruciali come la correttezza e la leggibilità.

In questa sezione vengono descritte le tecniche di interoperabilità seguenti:

-   D3D12 e D3D12 nello stesso dispositivo
-   D3D12 e D3D12 in dispositivi diversi
-   D3D12 e qualsiasi combinazione di D3D11, D3D10 o D2D nello stesso dispositivo
-   D3D12 e qualsiasi combinazione di D3D11, D3D10 o D2D in dispositivi diversi
-   D3D12 e GDI oppure D3D12 e D3D11 e GDI

## <a name="reasons-for-using-interop"></a>Motivi per l'utilizzo dell'interoperabilità

Ci sono diversi motivi per cui un'applicazione potrebbe volere D3D12 l'interoperabilità con altre API. Di seguito alcuni esempi:

-   Porting incrementale: si desidera trasferire un'intera applicazione da D3D10 o da D3D11 a D3D12, pur avendola funzionale a fasi intermedie del processo di porting (per abilitare il test e il debug).
-   Codice della casella nera: se si vuole lasciare una parte specifica di un'applicazione così com'è, durante il porting del resto del codice. Ad esempio, potrebbe non essere necessario trasferire gli elementi dell'interfaccia utente di un gioco.
-   Componenti non modificabili: è necessario usare i componenti che non sono di proprietà dell'applicazione, che non vengono scritti nei D3D12 di destinazione.
-   Un nuovo componente: se non si vuole trasferire l'intera applicazione, ma si vuole usare un nuovo componente scritto con D3D12.

Sono disponibili quattro tecniche principali per l'interoperabilità in D3D12:

-   Un'app può scegliere di fornire un elenco di comandi aperti a un componente, che registra alcuni comandi di rendering aggiuntivi in una destinazione di rendering già associata. Questa operazione equivale a fornire un contesto di dispositivo preparato a un altro componente in D3D11 ed è ideale per elementi come l'aggiunta di interfaccia utente/testo a un buffer nascosto già associato.
-   Un'app può scegliere di fornire una coda di comandi a un componente, insieme a una risorsa di destinazione desiderata. Questa operazione equivale a usare le API [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) o [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) in D3D11 per fornire un contesto di dispositivo pulito a un altro componente. Questo è il funzionamento dei componenti come D2D.
-   Un componente può optare per un modello in cui produce un elenco di comandi, potenzialmente in parallelo, che l'app è responsabile dell'invio in un secondo momento. È necessario fornire almeno una risorsa tra i limiti dei componenti. Questa stessa tecnica è disponibile in D3D11 usando contesti posticipati, sebbene le prestazioni in D3D12 siano più desiderate.
-   Ogni componente ha le proprie code e/o i dispositivi e l'app e i componenti devono condividere le risorse e le informazioni di sincronizzazione tra i limiti dei componenti. Si tratta di un aspetto simile a quello legacy `ISurfaceQueue` e alla [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)più moderna.

Le differenze tra questi scenari sono esattamente condivise tra i limiti dei componenti. Si presuppone che il dispositivo sia condiviso, ma poiché è fondamentalmente senza stato, non è rilevante. Gli oggetti chiave sono l'elenco dei comandi, la coda dei comandi, gli oggetti di sincronizzazione e le risorse. Ognuna di queste presenta complicazioni durante la condivisione.

### <a name="sharing-a-command-list"></a>Condivisione di un elenco di comandi

Per il metodo di interoperabilità più semplice è necessario condividere solo un elenco di comandi con una parte del motore. Una volta completate le operazioni di rendering, la proprietà dell'elenco dei comandi torna al chiamante. La proprietà dell'elenco di comandi può essere tracciata attraverso lo stack. Poiché gli elenchi di comandi sono a thread singolo, un'app non è in grado di eseguire un'operazione univoca o innovativa utilizzando questa tecnica.

### <a name="sharing-a-command-queue"></a>Condivisione di una coda di comandi

Probabilmente la tecnica più comune per più componenti che condividono un dispositivo nello stesso processo.

Quando la coda dei comandi è l'unità di condivisione, è necessario effettuare una chiamata al componente per informare che tutti gli elenchi di comandi in attesa devono essere inviati immediatamente alla coda dei comandi (ed è necessario sincronizzare tutte le code dei comandi interni). Questa operazione equivale all'API di [**scaricamento**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) d3d11 ed è l'unico modo in cui l'applicazione può inviare i propri elenchi di comandi o le primitive di sincronizzazione.

### <a name="sharing-sync-primitives"></a>Condivisione delle primitive di sincronizzazione

Il modello previsto per un componente che opera nei propri dispositivi e/o nelle code dei comandi consiste nell'accettare un handle condiviso o [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) e la coppia UInt64 al momento dell'inizio del lavoro, il quale rimarrà in attesa e quindi un secondo handle ID3D12Fence o Shared e la coppia UInt64 che segnalerà al termine di tutto il lavoro. Questo modello corrisponde all'implementazione corrente di [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) e della progettazione della sincronizzazione del modello di sincronizzazione di DWM/dxgi.

### <a name="sharing-resources"></a>Condivisione di risorse

La parte più complessa della scrittura di un'app D3D12 che sfrutta più componenti è la modalità di gestione delle risorse condivise tra i limiti dei componenti. Ciò è dovuto principalmente al concetto di stato delle risorse. Sebbene alcuni aspetti della progettazione dello stato delle risorse siano progettati per gestire la sincronizzazione all'interno dell'elenco dei comandi, altri hanno un impatto tra gli elenchi di comandi, influiscono sul layout delle risorse e sui set di operazioni validi o sulle caratteristiche delle prestazioni di accesso ai dati della risorsa.

Esistono due modelli di gestione di questa complicazione, che coinvolgono essenzialmente un contratto tra i componenti.

-   Il contratto può essere definito dallo sviluppatore del componente e documentato. Questa operazione può essere semplice quanto "la risorsa deve essere nello stato predefinito quando il lavoro viene avviato e verrà rimessa nello stato predefinito quando il lavoro viene eseguito" o potrebbe avere regole più complesse per consentire elementi come la condivisione di un buffer di profondità senza forzare la risoluzione della profondità intermedia.
-   Il contratto può essere definito dall'applicazione in fase di esecuzione, nel momento in cui la risorsa viene condivisa tra i limiti dei componenti. È costituito dalle stesse due informazioni: lo stato in cui si troverà la risorsa quando il componente inizia a utilizzarlo e lo stato in cui il componente deve lasciarlo al termine dell'operazione.

### <a name="choosing-an-interop-model"></a>Scelta di un modello di interoperabilità

Per la maggior parte delle applicazioni D3D12, la condivisione di una coda di comandi è probabilmente il modello ideale. Consente di completare la proprietà della creazione e dell'invio del lavoro, senza l'overhead aggiuntivo della memoria dovuto alla presenza di code ridondanti e senza l'impatto sulle prestazioni delle primitive di sincronizzazione della GPU.

La condivisione delle primitive di sincronizzazione è necessaria quando i componenti devono gestire diverse proprietà della coda, ad esempio il tipo o la priorità, oppure quando la condivisione deve estendere i limiti del processo.

La condivisione o la produzione di elenchi di comandi non è ampiamente usata esternamente da componenti di terze parti, ma può essere ampiamente usata nei componenti interni a un motore di gioco.

## <a name="interop-apis"></a>API di interoperabilità

Nell'argomento [Direct3D 11 su 12](./direct3d-11-on-12.md) viene illustrato l'utilizzo di gran parte della superficie dell'API correlata ai tipi di interoperabilità descritti in questo argomento.

Vedere anche il metodo [ID3D12Device:: CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) , che è possibile usare per condividere le superfici tra le API grafiche di Windows.

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni su Direct3D 12](directx-12-getting-started.md)
* [Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
* [D3D11On12](./direct3d-11-on-12.md)