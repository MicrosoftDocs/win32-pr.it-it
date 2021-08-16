---
title: Confronto tra l'accelerazione hardware Direct2D e GDI
description: Direct2D e GDI sono entrambe API di rendering 2D in modalità immediata ed entrambe offrono un certo grado di accelerazione hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa5fcb0f186915570d220a2807f816eae7a20fb393fbcd3113f6abf686fcd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826546"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Confronto tra l'accelerazione hardware Direct2D e GDI

[Direct2D](./direct2d-portal.md) e [GDI sono](/windows/desktop/gdi/windows-gdi) entrambe API di rendering 2D in modalità immediata ed entrambe offrono un certo grado di accelerazione hardware. Questo argomento illustra le differenze tra Direct2D e GDI, incluse le differenze passate e presenti nelle funzionalità di accelerazione hardware di entrambe le API.

Questo argomento include le parti seguenti:

-   [Differenze tra Direct2D e GDI](#differences-between-direct2d-and-gdi)
-   [Accelerazione hardware GDI e Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumento della complessità e delle dimensioni dei driver di visualizzazione](#increasing-complexity-and-size-of-display-drivers)
    -   [Difficoltà nella sincronizzazione degli spazi degli indirizzi globali del kernel e della sessione](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Gestione delle finestre composte](#composited-window-management)
-   [Rendering GDI in Windows 7](#gdi-rendering-in-windows-7)
-   [Accelerazione Direct2D e GDI a contrasto in Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Posizione delle risorse](#location-of-resources)
    -   [Metodo di rendering](#rendering-method)
    -   [Scalabilità](#scalability)
    -   [Posizione](#location-of-resources)
    -   [Disponibilità dell'accelerazione hardware](#availability-of-hardware-acceleration)
    -   [Modello di presentazione](#presentation-model)
-   [Conclusione](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Differenze tra Direct2D e GDI

[GDI](/windows/desktop/gdi/windows-gdi) esegue il rendering di geometrie opache con alias, ad esempio poligoni, ellissi e linee. Esegue il rendering di testo con alias e ClearType e può supportare la fusione della trasparenza tramite l'API AlphaBlend. Tuttavia, la gestione della trasparenza è incoerente e la maggior parte delle API GDI ignora semplicemente il canale alfa. Poche API GDI garantiscono ciò che il canale alfa conterrà dopo un'operazione. Ancora più importante, il rendering di GDI non viene mappato facilmente alle operazioni 3D e una GPU moderna esegue il rendering in modo più efficiente nella parte 3D del motore di rendering. Ad esempio, le linee con alias di [Direct2D](./direct2d-portal.md)sono progettate per essere implementate semplicemente come due triangoli sottoposti a rendering nella GPU, mentre GDI usa l'algoritmo di disegno a linee di Bresenham.

[Direct2D esegue](./direct2d-portal.md) il rendering di primitive opache, trasparenti, con alias e antialiasing. Le moderne ui usano spesso la trasparenza e l'animazione. Direct2D semplifica la creazione di un'interfaccia utente moderna perché ha garanzie rigorose sul modo in cui accetta ed esegue il rendering di contenuto trasparente e tutte le primitive vengono sottoposte a rendering usando l'accelerazione hardware. Direct2D non è un superset puro di [GDI:](/windows/desktop/gdi/windows-gdi)le primitive che sarebbero state irragionevolmente lente quando implementate in una GPU non sono presenti in Direct2D. Poiché Direct2D è stato creato con questa enfasi sull'accelerazione 3D, è anche facile da usare con Direct3D.

A partire Windows NT 4, [GDI](/windows/desktop/gdi/windows-gdi) è stato eseguito in modalità kernel. L'applicazione chiama GDI che chiama quindi la controparte in modalità kernel che passa le primitive al proprio modello di driver. Questo driver invia quindi i risultati al driver di visualizzazione in modalità kernel globale.

A partire Windows 2000, I driver GDI e [GDI](/windows/desktop/gdi/windows-gdi) sono stati eseguiti in uno spazio indipendente nel kernel denominato "spazio di sessione". Viene creato uno spazio indirizzi di sessione per ogni sessione di accesso e ogni istanza di GDI viene eseguita in modo indipendente in questo spazio di indirizzi distinto in modalità kernel. Direct2D, tuttavia, viene eseguito in modalità utente e passa i comandi di disegno tramite il driver Direct3D in modalità utente al driver in modalità kernel.

![figura 1 - direct2d rispetto a gdi](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Accelerazione hardware GDI e Direct2D

La differenza più importante tra [l'accelerazione hardware Direct2D](./direct2d-portal.md) [e GDI](/windows/desktop/gdi/windows-gdi) è la tecnologia sottostante che li guida. Direct2D è suddiviso in livelli su Direct3D e GDI ha un proprio modello di driver, L'interfaccia DDI (Device Driver Interface) GDI, che corrisponde alle primitive GDI. Il modello di driver Direct3D corrisponde al rendering dell'hardware di rendering 3D in una GPU. Quando è stato definito per la prima volta il DDI GDI, la maggior parte dell'hardware di accelerazione dello schermo ha come destinazione le primitive GDI. Nel corso del tempo, è stata posta sempre più enfasi sull'accelerazione del gioco 3D e meno sull'accelerazione dell'applicazione. Di conseguenza, l'API BitBlt era accelerata dall'hardware e la maggior parte delle altre operazioni GDI non lo erano.

In questo modo viene impostata la fase per una sequenza di modifiche al modo in cui [GDI](/windows/desktop/gdi/windows-gdi) esegue il rendering sulla visualizzazione. La figura seguente mostra come il rendering della visualizzazione GDI è cambiato da Windows XP a Windows 7.

![Figura 2 - Evoluzione del rendering dello schermo gdi](images/direct2d-vs-gdi2.png)

Sono stati inoltre apportati diversi fattori aggiuntivi che hanno causato modifiche al modello di driver [GDI,](/windows/desktop/gdi/windows-gdi) come illustrato di seguito.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumento della complessità e delle dimensioni dei driver di visualizzazione

I driver 3D sono diventati più complessi nel tempo. Il codice più complesso tende ad avere più difetti, rendendo vantaggioso che il driver esista in modalità utente in cui un bug del driver non può causare un riavvio del sistema. Come si può vedere nella figura precedente, il driver di visualizzazione è suddiviso in un componente in modalità utente complesso e in un componente in modalità kernel più semplice.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Difficoltà nella sincronizzazione degli spazi degli indirizzi globali del kernel e della sessione

In Windows XP, un driver di visualizzazione esiste in due spazi indirizzi diversi: spazio di sessione e spazio del kernel. Parti del driver devono rispondere a eventi come gli eventi di risparmio energia. Deve essere sincronizzato con lo stato del driver nello spazio degli indirizzi della sessione. Si tratta di un'attività difficile e può causare difetti quando i driver di visualizzazione tentano di gestire questi spazi di indirizzi distinti.

### <a name="composited-window-management"></a>Gestione delle finestre composte

Il Gestione finestre desktop (DWM), il gestore di finestre di composizione introdotto in Windows 7, esegue il rendering di tutte le finestre su superfici fuori schermo e quindi le compone insieme per essere visualizzate sullo schermo. Ciò richiede [che GDI](/windows/desktop/gdi/windows-gdi) sia in grado di eseguire il rendering su una superficie che verrà quindi sottoposta a rendering da Direct3D per la visualizzazione. Ciò ha rappresentato un problema nel modello di driver XP, poiché GDI e Direct3D erano stack di driver paralleli.

Di conseguenza, in Windows Vista, il driver di visualizzazione [DDI GDI](/windows/desktop/gdi/windows-gdi) è stato implementato come driver cdD (Canonical Display Driver) fornito da Microsoft che ha eseguito il rendering del contenuto GDI in una bitmap della memoria di sistema da componere sullo schermo.

## <a name="gdi-rendering-in-windows-7"></a>Rendering GDI in Windows 7

Il modello di driver usato in Windows Vista richiedeva che ogni [finestra GDI](/windows/desktop/gdi/windows-gdi) sia supportata sia da una superficie di memoria video che da una superficie di memoria di sistema. Ciò ha comportato l'uso della memoria di sistema per ogni finestra GDI.

Per questo motivo, [GDI](/windows/desktop/gdi/windows-gdi) è stato modificato di nuovo in Windows 7. . Invece di eseguire il rendering su una superficie di memoria di sistema, GDI è stato modificato per il rendering in un segmento di memoria di apertura. La memoria di apertura può essere aggiornata dalla superficie di memoria video che contiene il contenuto della finestra. GDI può eseguire il rendering nella memoria di apertura e il risultato può quindi essere restituito alla superficie della finestra. Poiché il segmento di memoria di apertura è indirizzabile dalla GPU, la GPU può accelerare questi aggiornamenti alla superficie di memoria video. Ad esempio, il rendering del testo, BitBlts, AlphaBlend, TransparentBlt e StretchBlt sono tutti accelerati in questi casi.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Accelerazione Direct2D e GDI a contrasto in Windows 7

[Direct2D](./direct2d-portal.md) e [GDI sono](/windows/desktop/gdi/windows-gdi) entrambe API di rendering in modalità immediata 2D e sono accelerate dall'hardware. Esistono tuttavia alcune differenze che rimangono in entrambe le API.

### <a name="location-of-resources"></a>Posizione delle risorse

[GDI](/windows/desktop/gdi/windows-gdi) mantiene le risorse, in particolare le bitmap, nella memoria di sistema per impostazione predefinita. [Direct2D](./direct2d-portal.md) mantiene le risorse nella memoria video sulla scheda video. Quando GDI deve aggiornare la memoria video, questa operazione deve essere eseguita sul bus, a meno che la risorsa non sia già nel segmento di memoria di apertura o se l'operazione può essere espressa direttamente. Al contrario, Direct2D può semplicemente tradurre le primitive in primitive Direct3D perché le risorse sono già nella memoria video.

### <a name="rendering-method"></a>Metodo di rendering

Per mantenere la compatibilità, [GDI](/windows/desktop/gdi/windows-gdi) esegue gran parte del rendering nella memoria di apertura usando la CPU. Al contrario, [Direct2D](./direct2d-portal.md) converte le chiamate api in primitive Direct3D e operazioni di disegno. Viene quindi eseguito il rendering del risultato nella GPU. Parte del rendering di GDI viene eseguito nella GPU quando la memoria di apertura viene copiata nella superficie di memoria video che rappresenta la finestra GDI.

### <a name="scalability"></a>Scalabilità

Le chiamate di rendering di [Direct2D](./direct2d-portal.md)sono tutti flussi di comando indipendenti per la GPU. Ogni factory Direct2D rappresenta un dispositivo Direct3D diverso. [GDI](/windows/desktop/gdi/windows-gdi) usa un flusso di comandi per tutte le applicazioni nel sistema. Il metodo di GDI può comportare un sovraccarico del contesto di rendering della GPU e della CPU.

### <a name="location"></a>Località

[Direct2D](./direct2d-portal.md) funziona interamente in modalità utente, incluso il run-time Direct3D e il driver Direct3D in modalità utente. Ciò consente di evitare arresti anomali del sistema causati da difetti del codice nel kernel. [GDI,](/windows/desktop/gdi/windows-gdi)tuttavia, ha la maggior parte delle funzionalità nello spazio di sessione in modalità kernel, con la superficie API in modalità utente.

### <a name="availability-of-hardware-acceleration"></a>Disponibilità dell'accelerazione hardware

[GDI](/windows/desktop/gdi/windows-gdi) è accelerato hardware in Windows XP e accelerato su Windows 7 quando il Gestione finestre desktop è in esecuzione e un driver WDDM 1.1 è in uso. [Direct2D](./direct2d-portal.md) è l'hardware accelerato in quasi tutti i driver WDDM e indica se DWM è in uso o meno. In Vista, GDI eseguirà sempre il rendering nella CPU.

### <a name="presentation-model"></a>Modello di presentazione

Quando Windows stata progettata per la prima volta, la memoria era insufficiente per consentire l'archiviazione di ogni finestra nella propria bitmap. Di conseguenza, [il rendering di GDI](/windows/desktop/gdi/windows-gdi) viene sempre eseguito logicamente direttamente sullo schermo, con diverse aree di ritaglio applicate per garantire che un'applicazione non eserciti il rendering all'esterno della relativa finestra. Nel modello [Direct2D](./direct2d-portal.md) il rendering di un'applicazione viene eseguito in un buffer nascosto e il risultato viene visualizzato al termine del disegno dell'applicazione. Ciò consente a Direct2D di gestire gli scenari di animazione in modo molto più fluido rispetto a GDI.

## <a name="conclusion"></a>Conclusione

Il [codice GDI](/windows/desktop/gdi/windows-gdi) esistente continuerà a funzionare correttamente Windows 7. Tuttavia, quando si scrive un nuovo codice per il rendering della grafica, è consigliabile prendere in considerazione [Direct2D,](./direct2d-portal.md) in quanto sfrutta meglio le GPU moderne.

 

 