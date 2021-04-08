---
title: App Direct2D multithreading
description: Descrive le procedure consigliate per la creazione di app Direct2D multithread.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/03/2020
ms.locfileid: "103734791"
---
# <a name="multithreaded-direct2d-apps"></a>App Direct2D multithreading

Se si sviluppano applicazioni [Direct2D](./direct2d-portal.md) , potrebbe essere necessario accedere alle risorse Direct2D da più di un thread. In altri casi, è consigliabile usare il multithreading per ottenere prestazioni migliori o una maggiore velocità di risposta, ad esempio l'uso di un thread per la visualizzazione dello schermo e di un thread separato per il rendering offline.

Questo argomento descrive le procedure consigliate per lo sviluppo di app [Direct2D](./direct2d-portal.md) multithreading con rendering [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ridotto. Gli errori software causati da problemi di concorrenza possono essere difficili da rilevare ed è utile pianificare i criteri di multithreading e seguire le procedure consigliate descritte di seguito.

> [!Note]  
> Se si accede a due risorse [Direct2D](./direct2d-portal.md) create da due diverse factory Direct2D a thread singolo, non si verificano conflitti di accesso finché i dispositivi [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) e i contesti di dispositivo sottostanti sono anche distinti. Quando si parla di "accesso alle risorse Direct2D" in questo articolo, significa semplicemente "accesso alle risorse Direct2D create dallo stesso dispositivo Direct2D", a meno che non sia specificato diversamente.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Sviluppo di app Thread-Safe che chiamano solo API Direct2D

È possibile creare un'istanza di factory [Direct2D](./direct2d-portal.md) multithreading. È possibile usare e condividere una factory multithreading e tutte le relative risorse da più di un thread, ma gli accessi a tali risorse (tramite chiamate Direct2D) vengono serializzati da Direct2D, quindi non si verificano conflitti di accesso. Se l'app chiama solo le API Direct2D, tale protezione viene eseguita automaticamente da Direct2D in un livello granulare con sovraccarico minimo. Il codice per creare una factory multithreading qui.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

Nell'immagine seguente viene illustrato il modo in cui [Direct2D](./direct2d-portal.md) serializza due thread che effettuano chiamate utilizzando solo l'API Direct2D.

![diagramma di due thread serializzati.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Sviluppo di applicazioni Direct2D Thread-Safe con chiamate Direct3D o DXGI minime

È più spesso che un'app [Direct2D](./direct2d-portal.md) esegue anche alcune chiamate a [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o dxgi. Ad esempio, un thread di visualizzazione verrà disegnato in Direct2D, quindi presenterà usando una [**catena di scambio DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

In questo caso, garantire la sicurezza dei thread è più complessa: alcune chiamate [Direct2D](./direct2d-portal.md) accedono indirettamente alle risorse [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) sottostanti, che potrebbero essere accessibili contemporaneamente da un altro thread che chiama Direct3D o dxgi. Poiché le chiamate Direct3D o DXGI sono fuori da le convenzioni Awareness and Control, è necessario creare una factory Direct2D multithreading, ma è necessario eseguire Mor per evitare conflitti di accesso.

Il diagramma mostra un conflitto di accesso alle risorse [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) a causa del thread T0 che accede indirettamente a una risorsa tramite una chiamata [Direct2D](./direct2d-portal.md) e T2 che accede alla stessa risorsa direttamente tramite una chiamata Direct3D o dxgi.

> [!Note]  
> La protezione dei thread fornita da [Direct2D](./direct2d-portal.md) (il blocco blu in questa immagine) non è utile in questo caso.

 

![diagramma di protezione thread.](images/multi-thread2.png)

Per evitare il conflitto di accesso alle risorse, è consigliabile acquisire in modo esplicito il blocco usato da [Direct2D](./direct2d-portal.md) per la sincronizzazione dell'accesso interno e applicare tale blocco quando un thread deve effettuare chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI che potrebbero causare conflitti di accesso, come illustrato di seguito. In particolare, è necessario prestare particolare attenzione al codice che usa le eccezioni o un sistema di primo in uscita in base ai codici restituiti HRESULT. Per questo motivo, è consigliabile usare un criterio di inizializzazione di RAII (acquisizione di risorse) per chiamare i metodi [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) .

> [!Note]  
> È importante associare le chiamate ai metodi [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) . in caso contrario, l'app può essere bloccata in deadlock.

 

Il codice mostra un esempio di quando bloccare e quindi sbloccare le chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o dxgi.


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
> Alcune chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI (in particolare [**IDXGISwapChain::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)reinviate) possono acquisire i blocchi e/o i callback del trigger nel codice della funzione o del metodo chiamante. È necessario tenere presente questo comportamento e assicurarsi che tale comportamento non provochi deadlock. Per altre informazioni, vedere l'argomento [Panoramica di DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![diagramma di blocco del thread Direct2D e Direct3D.](images/multi-thread3.png)

Quando si usano i metodi [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , le chiamate sono protette dal [Direct2D](./direct2d-portal.md) automatico e dal blocco esplicito, quindi l'app non raggiunge il conflitto di accesso.

Esistono altri approcci per risolvere questo problema. Tuttavia, si consiglia di proteggere in modo esplicito le chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI con il blocco [Direct2D](./direct2d-portal.md) , perché in genere fornisce prestazioni migliori in quanto protegge la concorrenza a un livello più preciso e con un sovraccarico inferiore nella copertura di le convenzioni.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Verifica dell'atomicità delle operazioni con stato

Sebbene le funzionalità di thread safety di [DirectX](/previous-versions//ee663301(v=vs.85)) contribuiscano a garantire che non vengano effettuate due singole chiamate API contemporaneamente, è necessario assicurarsi anche che i thread che eseguono chiamate API con stato non interferiscano tra loro. Ecco un esempio.

1.  Ci sono due righe di testo di cui si vuole eseguire il rendering sia sullo schermo (dal thread 0) sia sullo schermo (dal thread 1): la riga \# 1 è "a è maggiore" e \# la riga 2 è "than B", entrambe che verranno disegnate usando un pennello nero a tinta unita.
2.  Il thread 1 disegna la prima riga di testo.
3.  Il thread 0 reagisce a un input dell'utente, aggiorna entrambe le righe di testo a "B" e "rispettivamente" e "di un" e ha modificato il colore del pennello in rosso continuo per il proprio disegno;
4.  Il thread 1 continua a disegnare la seconda riga di testo, che ora è "Than A", con il pennello di colore rosso;
5.  Infine, si ottengono due righe di testo nella destinazione del disegno fuori schermo: "A è maggiore" in nero e "di a" in rosso.

![diagramma dei thread su schermo.](images/multi-thread4.png)

Nella riga superiore, il thread 0 disegna con le stringhe di testo correnti e il pennello nero corrente. Il thread 1 termina solo il disegno fuori schermo sulla metà superiore.

Nella riga intermedia, il thread 0 risponde all'interazione dell'utente, aggiorna le stringhe di testo e il pennello, quindi aggiorna la schermata. A questo punto, il thread 1 è bloccato. Nella riga inferiore, il rendering finale fuori schermo dopo il thread 1 riprende a disegnare la metà inferiore con un pennello modificato e una stringa di testo modificata.

Per risolvere questo problema, è consigliabile disporre di un contesto separato per ogni thread, in modo che:

-   È necessario creare una copia del contesto di dispositivo in modo che le risorse modificabili, ad esempio le risorse che possono variare durante la visualizzazione o la stampa, come il contenuto di testo o il pennello tinta unita nell'esempio, non cambino quando si esegue il rendering. In questo esempio, è consigliabile mantenere una copia di queste due righe di testi e il pennello del colore prima di creare. In questo modo, si garantisce che ogni thread abbia contenuto completo e coerente da creare e presentare.
-   È consigliabile condividere risorse di peso elevato, come bitmap e grafici con effetti complessi, che vengono inizializzate una volta e quindi mai modificate tra i thread per migliorare le prestazioni.
-   È possibile condividere risorse leggere (ad esempio, pennelli a tinta unita e formati di testo) che vengono inizializzate una sola volta e non vengono mai modificate tra i thread

## <a name="summary"></a>Riepilogo

Quando si sviluppano applicazioni [Direct2D](./direct2d-portal.md) multithreading, è necessario creare una factory Direct2D multithreading, quindi derivare tutte le risorse Direct2D da tale factory. Se un thread effettuerà chiamate [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI, è anche necessario acquisire in modo esplicito, quindi applicare il blocco Direct2D per proteggere le chiamate Direct3D o dxgi. Inoltre, è necessario garantire l'integrità del contesto con una copia delle risorse modificabili per ogni thread.
