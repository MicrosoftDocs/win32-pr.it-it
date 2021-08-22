---
title: App Direct2D multithreading
description: Descrive le procedure consigliate per la creazione di app Direct2D multithreading.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5710435f263e7b0f735581e03416f1d01733711429ad95b3ed25e473aca6d936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636421"
---
# <a name="multithreaded-direct2d-apps"></a>App Direct2D multithreading

Se si [sviluppano app Direct2D,](./direct2d-portal.md) potrebbe essere necessario accedere alle risorse Direct2D da più thread. In altri casi, è possibile usare il multithreading per ottenere prestazioni migliori o velocità di risposta migliori, ad esempio usando un thread per la visualizzazione dello schermo e un thread separato per il rendering offline.

Questo argomento descrive le procedure consigliate per lo sviluppo di app [Direct2D](./direct2d-portal.md) multithreading senza rendering [Direct3D.](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) I difetti software causati da problemi di concorrenza possono essere difficili da rilevare ed è utile pianificare i criteri di multithreading e seguire le procedure consigliate descritte qui.

> [!Note]  
> Se si accede a due risorse [Direct2D](./direct2d-portal.md) create da due factory Direct2D a thread singolo diverse, non si verificano conflitti di accesso, purché siano distinti anche i dispositivi [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) sottostanti e i contesti di dispositivo. Quando si parla di "accesso alle risorse Direct2D" in questo articolo, significa effettivamente "accesso alle risorse Direct2D create dallo stesso dispositivo Direct2D" se non diversamente specificato.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Sviluppo Thread-Safe app che chiamano solo API Direct2D

È possibile creare un'istanza della factory [Direct2D](./direct2d-portal.md) multithreading. È possibile usare e condividere una factory multithreading e tutte le relative risorse da più thread, ma gli accessi a tali risorse (tramite chiamate Direct2D) vengono serializzati da Direct2D, quindi non si verificano conflitti di accesso. Se l'app chiama solo LE API Direct2D, tale protezione viene eseguita automaticamente da Direct2D in un livello granulare con sovraccarico minimo. Il codice per creare una factory multithreading qui.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

L'immagine seguente mostra come [Direct2D](./direct2d-portal.md) serializza due thread che effettuano chiamate usando solo l'API Direct2D.

![Diagramma di due thread serializzati.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Sviluppo Thread-Safe app Direct2D con chiamate Direct3D o DXGI minime

Spesso un'app [Direct2D](./direct2d-portal.md) effettua anche alcune [chiamate Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI. Ad esempio, un thread di visualizzazione disemplierà in Direct2D e quindi presenterà usando una [**catena di scambio DXGI.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)

In questo caso, garantire la thread safety è più complicato: alcune chiamate [Direct2D](./direct2d-portal.md) accedono indirettamente alle risorse [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) sottostanti, a cui può accedere contemporaneamente un altro thread che chiama Direct3D o DXGI. Poiché tali chiamate Direct3D o DXGI non sono sensibili e controllate da Direct2D, è necessario creare una factory Direct2D multithreading, ma è necessario eseguire alcune operazioni per evitare conflitti di accesso.

Il diagramma seguente mostra un conflitto di accesso alle risorse [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) causato dal thread T0 che accede indirettamente a una risorsa tramite una chiamata [Direct2D](./direct2d-portal.md) e T2 che accede alla stessa risorsa direttamente tramite una chiamata Direct3D o DXGI.

> [!Note]  
> La protezione dei thread [fornita da Direct2D](./direct2d-portal.md) (il blocco blu in questa immagine) non è utile in questo caso.

 

![Diagramma di protezione dei thread.](images/multi-thread2.png)

Per evitare conflitti di accesso alle risorse, è consigliabile acquisire in modo esplicito il blocco utilizzato da [Direct2D](./direct2d-portal.md) per la sincronizzazione dell'accesso interno e applicare tale blocco quando un thread deve effettuare chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI che potrebbero causare conflitti di accesso, come illustrato di seguito. In particolare, è necessario fare particolare attenzione al codice che usa eccezioni o a un sistema in fase iniziale basato sui codici restituiti HRESULT. Per questo motivo, è consigliabile usare un modello RAII (Resource Acquisition Is Initialization) per chiamare i [**metodi Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) [**e Leave.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave)

> [!Note]  
> È importante associare le chiamate ai metodi [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) altrimenti l'app può deadlock.

 

Il codice seguente illustra un esempio di quando bloccare e quindi sbloccare le [chiamate Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI.


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> Alcune chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI (in particolare [**IDXGISwapChain::P resent)**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)possono acquisire blocchi e/o attivare callback nel codice della funzione o del metodo chiamante. È necessario tenere presente questo aspetto e assicurarsi che tale comportamento non causa deadlock. Per altre informazioni, vedere l'argomento [Panoramica di DXGI.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

 

![Diagramma di blocco dei thread direct2d e direct3d.](images/multi-thread3.png)

Quando si usano i [**metodi Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) le chiamate sono protette da [Direct2D](./direct2d-portal.md) automatico e dal blocco esplicito, in modo che l'app non sia in conflitto di accesso.

Esistono altri approcci per risolvere questo problema. Tuttavia, è consigliabile proteggere in modo esplicito le chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI con il blocco [Direct2D](./direct2d-portal.md) perché in genere offre prestazioni migliori perché protegge la concorrenza a un livello molto più fine e con un sovraccarico inferiore sotto la copertura di Direct2D.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Verifica dell'atomicità delle operazioni con stato

Anche se le funzionalità di thread safety di [DirectX](/previous-versions//ee663301(v=vs.85)) consentono di garantire che non vengono eseguite contemporaneamente due singole chiamate API, è necessario anche assicurarsi che i thread che effettuano chiamate API con stato non interferiscano l'uno con l'altro. Ecco un esempio.

1.  Ci sono due righe di testo di cui si vuole eseguire il rendering sia sullo schermo (per Thread 0) che fuori schermo (da Thread 1): la riga 1 è "A è maggiore" e la riga \# \# 2 è "di B", entrambe disegnate usando un pennello nero a tinta unita.
2.  Il thread 1 disegna la prima riga di testo.
3.  Il thread 0 reagisce a un input dell'utente, aggiorna entrambe le righe di testo rispettivamente a "B è più piccolo" e "A" e modifica il colore del pennello in rosso a tinta unita per il proprio disegno;
4.  Il thread 1 continua a disegnare la seconda riga di testo, che ora è "di A", con il pennello di colore rosso;
5.  Infine, si ottengono due righe di testo sulla destinazione di disegno fuori schermo: "A è maggiore" in nero e "than A" in rosso.

![diagramma dei thread su e fuori schermo.](images/multi-thread4.png)

Nella riga superiore Thread 0 disegna con le stringhe di testo correnti e il pennello nero corrente. Il thread 1 termina solo il disegno fuori schermo nella metà superiore.

Nella riga centrale, thread 0 risponde all'interazione dell'utente, aggiorna le stringhe di testo e il pennello, quindi aggiorna la schermata. A questo punto, il thread 1 è bloccato. Nella riga inferiore il rendering finale fuori schermo dopo thread 1 riprende a disegnare la metà inferiore con un pennello modificato e una stringa di testo modificata.

Per risolvere questo problema, è consigliabile avere un contesto separato per ogni thread, in modo che:

-   È consigliabile creare una copia del contesto di dispositivo in modo che le risorse modificabili,ad esempio le risorse che possono variare durante la visualizzazione o la stampa, ad esempio il contenuto del testo o il pennello a tinta unita nell'esempio, non cambino quando si esegue il rendering. In questo esempio è necessario mantenere una copia di queste due righe di testo e il pennello colore prima di disegnare. In questo modo, si garantisce che ogni thread abbia contenuto completo e coerente da disegnare e presentare.
-   È consigliabile condividere risorse complesse, ad esempio bitmap e grafici degli effetti complessi, inizializzate una sola volta e quindi mai modificate tra thread per migliorare le prestazioni.
-   È possibile condividere risorse leggere (ad esempio pennelli a tinta unita e formati di testo) inizializzate una sola volta e quindi mai modificate tra thread o meno

## <a name="summary"></a>Riepilogo

Quando si sviluppano app [Direct2D](./direct2d-portal.md) multithreading, è necessario creare una factory Direct2D multithread e quindi derivare tutte le risorse Direct2D da tale factory. Se un thread effettua [chiamate Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI, è anche necessario acquisire in modo esplicito il blocco Direct2D per proteggere tali chiamate Direct3D o DXGI. È inoltre necessario garantire l'integrità del contesto con una copia delle risorse modificabili per ogni thread.
