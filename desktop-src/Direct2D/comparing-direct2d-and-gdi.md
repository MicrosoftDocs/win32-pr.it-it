---
title: Confronto dell'accelerazione hardware Direct2D e GDI
description: Direct2D e GDI sono sia API di rendering 2D in modalità immediata che offrono un certo grado di accelerazione hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337639"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Confronto dell'accelerazione hardware Direct2D e GDI

[Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) sono sia API di rendering 2D in modalità immediata che offrono un certo grado di accelerazione hardware. In questo argomento vengono esaminate le differenze tra Direct2D e GDI, incluse le differenze precedenti e presenti nelle funzionalità di accelerazione hardware di entrambe le API.

Questo argomento include le parti seguenti:

-   [Differenze tra Direct2D e GDI](#differences-between-direct2d-and-gdi)
-   [Accelerazione hardware GDI e Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumento della complessità e della dimensione dei driver di visualizzazione](#increasing-complexity-and-size-of-display-drivers)
    -   [Problemi di sincronizzazione degli spazi di indirizzi del kernel e della sessione](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Gestione della finestra composita](#composited-window-management)
-   [Rendering GDI in Windows 7](#gdi-rendering-in-windows-7)
-   [Contrasto dell'accelerazione Direct2D e GDI in Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Percorso delle risorse](#location-of-resources)
    -   [Metodo di rendering](#rendering-method)
    -   [Scalabilità](#scalability)
    -   [Posizione](#location-of-resources)
    -   [Disponibilità dell'accelerazione hardware](#availability-of-hardware-acceleration)
    -   [Modello di presentazione](#presentation-model)
-   [Conclusione](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Differenze tra Direct2D e GDI

[GDI](/windows/desktop/gdi/windows-gdi) esegue il rendering di geometrie opache e con alias, ad esempio poligoni, ellissi e linee. Esegue il rendering del testo con alias e ClearType e può supportare la fusione della trasparenza tramite l'API AlphaBlend. Tuttavia, la gestione della trasparenza è incoerente e la maggior parte delle API GDI ignora semplicemente il canale alfa. Poche API GDI garantiscono ciò che il canale alfa conterrà dopo un'operazione. Ancora più importante, il rendering di GDI non è facilmente mappato alle operazioni 3D e una GPU moderna risulta più efficiente sulla parte 3D del motore di rendering. Ad esempio, le righe con alias di [Direct2D](./direct2d-portal.md)sono progettate per essere implementate semplicemente come due triangoli sottoposti a rendering sulla GPU, mentre GDI USA l'algoritmo di disegno a linee di Bresenham.

[Direct2D](./direct2d-portal.md) rende le primitive opache, trasparenti, con alias e con alias. Le interfacce utente moderne spesso usano la trasparenza e l'animazione. Direct2D semplifica la creazione di un'interfaccia utente moderna, poiché presenta una rigida garanzia sulla modalità di accettazione e rendering del contenuto trasparente e viene eseguito il rendering di tutte le primitive usando l'accelerazione hardware. Direct2D non è un superset puro di [GDI](/windows/desktop/gdi/windows-gdi): primitive che sarebbe stato ragionevolmente lento quando l'implementazione in una GPU non è presente in Direct2D. Poiché Direct2D è stato creato con questa enfasi sull'accelerazione 3D, è anche facile da usare con Direct3D.

Poiché Windows NT 4, [GDI](/windows/desktop/gdi/windows-gdi) è stato eseguito in modalità kernel. L'applicazione chiama GDI, che quindi chiama la controparte della modalità kernel che passa le primitive al proprio modello di driver. Questo driver invia quindi i risultati al driver di visualizzazione in modalità kernel globale.

A partire da Windows 2000, [GDI](/windows/desktop/gdi/windows-gdi) e i driver GDI sono stati eseguiti in uno spazio indipendente nel kernel denominato "spazio sessione". Uno spazio di indirizzi della sessione viene creato per ogni sessione di accesso e ogni istanza di GDI viene eseguita in modo indipendente in questo spazio di indirizzi in modalità kernel distinto. Direct2D, tuttavia, viene eseguito in modalità utente e passa i comandi di disegno tramite il driver Direct3D in modalità utente al driver in modalità kernel.

![Figura 1-Direct2D rispetto a GDI](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Accelerazione hardware GDI e Direct2D

La differenza più importante tra l'accelerazione hardware [Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) è la tecnologia sottostante che li gestisce. Direct2D è sovrapposto al primo Direct3D e GDI ha il proprio modello di driver, l'interfaccia DDI (Device Driver Interface) GDI, che corrisponde alle primitive GDI. Il modello di driver Direct3D corrisponde a ciò che l'hardware di rendering 3D in una GPU esegue il rendering. Quando l'interfaccia DDI GDI è stata definita per la prima volta, la maggior parte Visualizza l'hardware di accelerazione di destinazione delle primitive GDI Nel corso del tempo, la maggior enfasi è stata concentrata sull'accelerazione del gioco 3D e meno sull'accelerazione dell'applicazione. Di conseguenza, l'API BitBlt è stata accelerata dall'hardware e la maggior parte delle altre operazioni GDI non lo era.

Questa operazione consente di impostare la fase per una sequenza di modifiche apportate al rendering di [GDI](/windows/desktop/gdi/windows-gdi) nella visualizzazione. Nella figura seguente viene illustrato come il rendering della visualizzazione GDI sia stato modificato da Windows XP a Windows 7.

![Figura 2-evoluzione del rendering della visualizzazione GDI](images/direct2d-vs-gdi2.png)

Sono stati inoltre introdotti alcuni fattori aggiuntivi che hanno causato modifiche al modello di driver [GDI](/windows/desktop/gdi/windows-gdi) , come illustrato di seguito.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumento della complessità e della dimensione dei driver di visualizzazione

i driver 3D sono diventati più complessi nel tempo. Il codice più complesso tende a avere più difetti che rendono vantaggioso il driver in modalità utente in cui un bug del driver non può causare un riavvio del sistema. Come si può notare nella figura precedente, il driver di visualizzazione è diviso in un componente in modalità utente complesso e un componente in modalità kernel più semplice.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Problemi di sincronizzazione degli spazi di indirizzi del kernel e della sessione

In Windows XP, un driver di visualizzazione è presente in due spazi di indirizzi diversi: spazio della sessione e spazio del kernel. Parti del driver devono rispondere a eventi come gli eventi di risparmio energia. Questo deve essere sincronizzato con lo stato del driver nello spazio degli indirizzi della sessione. Si tratta di un'attività difficile che può causare errori quando i driver visualizzati tentano di gestire questi spazi di indirizzi distinti.

### <a name="composited-window-management"></a>Gestione della finestra composita

Il Gestione finestre desktop (DWM), la funzionalità di gestione delle finestre di composizione introdotta in Windows 7, esegue il rendering di tutte le finestre in superficie fuori schermo e quindi le compone insieme per essere visualizzate sullo schermo. A tale scopo è necessario che [GDI](/windows/desktop/gdi/windows-gdi) sia in grado di eseguire il rendering in una superficie che verrà quindi sottoposta a rendering da Direct3D per la visualizzazione. Si è verificato un problema nel modello di driver XP, perché GDI e Direct3D erano stack di driver paralleli.

Di conseguenza, in Windows Vista, il driver per la visualizzazione del dispositivo [GDI](/windows/desktop/gdi/windows-gdi) DDI è stato implementato come il driver di visualizzazione canonica fornito da Microsoft che ha eseguito il rendering del contenuto GDI in una bitmap di memoria di sistema da comporre sullo schermo.

## <a name="gdi-rendering-in-windows-7"></a>Rendering GDI in Windows 7

Il modello di driver utilizzato in Windows Vista richiede che ogni finestra [GDI](/windows/desktop/gdi/windows-gdi) sia supportata da una superficie di memoria video e da una superficie di memoria di sistema. Ciò ha comportato la memoria di sistema utilizzata per ogni finestra GDI.

Per questo motivo, [GDI](/windows/desktop/gdi/windows-gdi) è stato nuovamente modificato in Windows 7. . Anziché eseguire il rendering in una superficie di memoria di sistema, GDI è stato modificato per eseguire il rendering in un segmento di memoria di apertura. La memoria di apertura può essere aggiornata dall'area di memoria video che contiene il contenuto della finestra. GDI è in grado di eseguire il rendering alla memoria di apertura e il risultato può quindi essere restituito all'area della finestra. Poiché il segmento di memoria di apertura è indirizzabile dalla GPU, la GPU può accelerare questi aggiornamenti alla superficie di memoria del video. In questi casi, ad esempio, il rendering del testo, BitBlts, AlphaBlend, TransparentBlt e StretchBlt sono accelerati.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Contrasto dell'accelerazione Direct2D e GDI in Windows 7

[Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) sono entrambe API per il rendering in modalità immediata 2D e sono con accelerazione hardware. Tuttavia, esistono alcune differenze che rimangono in entrambe le API.

### <a name="location-of-resources"></a>Percorso delle risorse

Per impostazione predefinita, [GDI](/windows/desktop/gdi/windows-gdi) mantiene le risorse, in particolare bitmap, nella memoria di sistema. [Direct2D](./direct2d-portal.md) mantiene le risorse nella memoria video sulla scheda schermo. Quando GDI deve aggiornare la memoria video, questa operazione deve essere eseguita sul bus, a meno che la risorsa non sia già nel segmento di memoria di apertura o se l'operazione può essere espressa direttamente. Al contrario, Direct2D può semplicemente tradurre le primitive nelle primitive Direct3D perché le risorse si trovano già nella memoria video.

### <a name="rendering-method"></a>Metodo di rendering

Per mantenere la compatibilità, [GDI](/windows/desktop/gdi/windows-gdi) esegue una parte notevole del rendering della memoria di apertura mediante la CPU. Al contrario, [Direct2D](./direct2d-portal.md) converte le chiamate API nelle primitive Direct3D e nelle operazioni di disegno. Il risultato viene quindi sottoposto a rendering nella GPU. Il rendering di GDI? s viene eseguito sulla GPU quando la memoria di apertura viene copiata nella superficie di memoria del video che rappresenta la finestra GDI.

### <a name="scalability"></a>Scalabilità

Le chiamate di rendering di [Direct2D](./direct2d-portal.md)sono tutti flussi di comandi indipendenti alla GPU. Ogni factory Direct2D rappresenta un dispositivo Direct3D diverso. [GDI](/windows/desktop/gdi/windows-gdi) utilizza un flusso di comandi per tutte le applicazioni nel sistema. Il metodo GDI può comportare un sovraccarico del contesto di rendering della GPU e della CPU.

### <a name="location"></a>Location

[Direct2D](./direct2d-portal.md) funziona interamente in modalità utente, inclusi il runtime Direct3D e il driver Direct3D in modalità utente. Ciò consente di evitare arresti anomali del sistema causati da difetti del codice nel kernel. [GDI](/windows/desktop/gdi/windows-gdi), tuttavia, ha la maggior parte delle funzionalità nello spazio di sessione in modalità kernel, con la relativa superficie API in modalità utente.

### <a name="availability-of-hardware-acceleration"></a>Disponibilità dell'accelerazione hardware

[GDI](/windows/desktop/gdi/windows-gdi) viene accelerato in Windows XP e accelerato in Windows 7 quando il Gestione finestre desktop è in esecuzione e un driver WDDM 1,1 è in uso. [Direct2D](./direct2d-portal.md) viene accelerato in quasi tutti i driver WDDM e se DWM è in uso o meno. In vista, GDI eseguirà sempre il rendering sulla CPU.

### <a name="presentation-model"></a>Modello di presentazione

Quando Windows è stato progettato per la prima volta, non era disponibile memoria sufficiente per consentire l'archiviazione di ogni finestra nella relativa bitmap. Di conseguenza, [GDI](/windows/desktop/gdi/windows-gdi) viene sempre sottoposto a rendering logico direttamente sullo schermo, con diverse aree di ritaglio applicate per garantire che un'applicazione non venga sottoposta a rendering al di fuori della finestra. Nel modello [Direct2D](./direct2d-portal.md) un'applicazione esegue il rendering in un buffer nascosto e il risultato viene visualizzato al termine del disegno dell'applicazione. In questo modo Direct2D può gestire scenari di animazione molto più fluidi rispetto a GDI.

## <a name="conclusion"></a>Conclusione

Il codice [GDI](/windows/desktop/gdi/windows-gdi) esistente continuerà a funzionare correttamente in Windows 7. Tuttavia, quando si scrive un nuovo codice di rendering della grafica, è necessario considerare [Direct2D](./direct2d-portal.md) , perché sfrutta al meglio le GPU moderne.

 

 