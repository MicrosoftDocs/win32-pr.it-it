---
title: Introduzione a DirectML
description: Direct Machine Learning (DirectML) è un'API di basso livello per Machine Learning (ML).
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104559"
---
# <a name="introduction-to-directml"></a>Introduzione a DirectML

## <a name="summary"></a>Riepilogo

Direct Machine Learning (DirectML) è un'API di basso livello per Machine Learning (ML). Le primitive di Machine Learning con accelerazione hardware (detti operatori) sono i blocchi predefiniti di DirectML. Da questi blocchi predefiniti è possibile sviluppare tecniche di apprendimento automatico come il ridimensionamento, l'anti-aliasing e il trasferimento dello stile, a un nome ma solo alcuni. Denoising e super-risoluzione, ad esempio, consentono di ottenere effetti raytraced impressionanti con un minor numero di raggi per pixel.

È possibile integrare i carichi di lavoro del machine learning nel gioco, nel motore, nel middleware, nel back-end o in un'altra applicazione. DirectML dispone di un flusso di lavoro e di un'interfaccia di programmazione di tipo DirectX 12 (C++ nativo, Nano-COM) e supportato da tutti i componenti hardware compatibili con DirectX 12. Per le applicazioni di esempio DirectML, incluso un esempio di un'applicazione DirectML minima, vedere [applicazioni di esempio DirectML](dml-min-app.md).

DirectML è stato introdotto in Windows 10, versione 1903 e nella versione corrispondente del Windows SDK.

## <a name="is-directml-appropriate-for-my-project"></a>DirectML è appropriato per il progetto?

DirectML è un componente di [Windows Machine Learning](/windows/ai) Umbrella. L'API WinML di livello superiore è principalmente incentrata sul modello, con il flusso di lavoro Load-bind-Evaluate. Tuttavia, per sfruttare al meglio il silicio, domini come giochi e motori richiedono in genere un livello di astrazione inferiore e un livello superiore di controllo dello sviluppatore. Se si contano i millisecondi e si spremeno i tempi dei fotogrammi, DirectML soddisferà le esigenze di machine learning.

Per scenari affidabili in tempo reale, a prestazioni elevate, a bassa latenza e/o con vincoli di risorse, usare DirectML (anziché WinML). È possibile integrare DirectML direttamente nel motore esistente o nella pipeline di rendering. In alternativa, a un livello superiore per i Framework e il middleware personalizzati di Machine Learning, DirectML può offrire un back-end a prestazioni elevate in Windows.

WinML viene implementato utilizzando DirectML come uno dei relativi backend.

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>Operazioni eseguite da DirectML; e quali operazioni è *necessario eseguire* come sviluppatore?

DirectML esegue in modo efficiente i singoli livelli del modello di inferenza sulla GPU (o sui core di accelerazione AI, se presenti). Ogni livello è un operatore e DirectML fornisce una libreria di operatori primitivi di Machine Learning con accelerazione hardware di basso livello. Questi operatori hanno ottimizzazioni specifiche per l'hardware e per l'architettura progettate in a loro (più avanti nella sezione [perché DirectML esegue correttamente?](#why-does-directml-perform-so-well)). Allo stesso tempo, lo sviluppatore vedrà una singola interfaccia indipendente dal fornitore per l'esecuzione di tali operatori.

La libreria di operatori in DirectML fornisce tutte le operazioni usuali che ci si aspetterebbe di poter usare in un carico di lavoro di machine learning.

- Operatori di attivazione, ad esempio **Linear**, **ReLU**, **Sigma**, **tanh** e altro ancora.
- Operatori per elementi, ad esempio **Add**, **Exp**, **log**, **Max**, **min**, **Sub** e altro ancora.
- Operatori di convoluzione, ad esempio **convoluzione** 2D e 3D e altro ancora.
- Operatori di riduzione, ad esempio **argmin**, **Average**, **L2**, **Sum** e altro ancora.
- Operatori di pooling, ad esempio **Average**, **LP** e **Max**.
- Operatori Neural Network (NN), ad esempio **GEMM**, **gru**, **LSTM** e **RNN**.
- E molti altri.

Per ottenere prestazioni ottimali e non pagare per ciò che non si usa, DirectML mette il controllo in mano come sviluppatore sulla modalità di esecuzione del carico di lavoro di Machine Learning sull'hardware. Scoprire quali operatori eseguire e quando è responsabilità dello sviluppatore. Le attività che si lasciano a discrezione includono: la trascrizione del modello; semplificazione e ottimizzazione dei livelli; caricamento dei pesi; allocazione delle risorse, associazione, gestione della memoria (analogamente a Direct3D 12); ed esecuzione del grafo.

Si conservano informazioni di alto livello sui grafici (è possibile impostare il modello a livello di codice direttamente oppure è possibile scrivere un caricatore del modello personalizzato). È possibile progettare un modello di scalabilità orizzontale, ad esempio, usando diversi livelli ciascuno degli operatori di **ricampionamento**, **convoluzione**, **normalizzazione** e **attivazione** . Con una certa familiarità, una pianificazione attenta e una gestione delle barriere, è possibile estrarre il massimo parallelismo e le prestazioni dell'hardware. Se si sta sviluppando un gioco, l'accurata gestione delle risorse e il controllo sulla pianificazione consentono di Interleave sui carichi di lavoro di machine learning e sul lavoro di rendering tradizionale per saturare la GPU.

## <a name="whats-the-high-level-directml-workflow"></a>Qual è il flusso di lavoro DirectML di alto livello?

Ecco la ricetta generale per il modo in cui si prevede di usare DirectML. All'interno delle due fasi principali di inizializzazione ed esecuzione, è possibile registrare il lavoro in elenchi di comandi e quindi eseguirli in una coda.

### <a name="initialization"></a>Inizializzazione

1. Creare le risorse Direct3D 12 &mdash; il dispositivo Direct3D 12, la coda di comandi, l'elenco dei comandi e le risorse come gli heap dei descrittori.
2. Poiché si sta effettuando l'inferenza di machine learning oltre al carico di lavoro di rendering, creare risorse DirectML &mdash; il dispositivo DirectML e le istanze dell'operatore. Se si dispone di un modello di apprendimento automatico in cui è necessario eseguire un particolare tipo di convoluzione con una determinata dimensione del tensore di filtro con un particolare tipo di dati, questi sono tutti parametri nell'operatore di **convoluzione** di DirectML.
3. DirectML registra il lavoro negli elenchi di comandi Direct3D 12. Quindi, una volta completata l'inizializzazione, si registra l'associazione e l'inizializzazione di (ad esempio) l'operatore di convoluzione nell'elenco dei comandi. Quindi, chiudere ed eseguire l'elenco dei comandi nella coda come di consueto.

### <a name="execution"></a>Esecuzione

1. Caricare i tensori di peso in risorse. Un tensore in DirectML viene rappresentato usando una risorsa Direct3D 12 normale. Se, ad esempio, si desidera caricare i dati relativi al peso nella GPU, è possibile eseguire questa operazione esattamente come per qualsiasi altra risorsa Direct3D 12 (usare un heap di caricamento o la coda di copia).
2. A questo punto, è necessario associare tali risorse di Direct3D 12 ai tensori di input e di output. Registra nel comando elenca l'associazione e l'esecuzione degli operatori.
3. Chiudere ed eseguire l'elenco dei comandi.

Analogamente a Direct3D 12, la durata delle risorse e la sincronizzazione sono responsabilità dell'utente. Ad esempio, non rilasciare gli oggetti DirectML almeno fino a quando non è stata completata l'esecuzione nella GPU.

## <a name="why-does-directml-perform-so-well"></a>Perché DirectML viene eseguito correttamente?

C'è un buon motivo per cui non è sufficiente scrivere un proprio operatore di convoluzione (ad esempio) come HLSL in un [compute shader](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline). Il vantaggio dell'uso di DirectML è che &mdash; , oltre a risparmiare il lavoro di homebrewing per la propria soluzione, &mdash; offre la possibilità di ottenere prestazioni decisamente migliori rispetto a quanto possibile con uno shader di calcolo per utilizzo generico scritto manualmente per qualcosa di simile a **convoluzione** o **LSTM**.

DirectML realizza questa operazione in parte grazie alla funzionalità per i metacomandi Direct3D 12. I metacomandi espongono una black box di funzionalità fino a DirectML, che consente ai fornitori di hardware di fornire l'accesso DirectML alle ottimizzazioni specifiche dell'architettura e dell'hardware del fornitore. Più operatori &mdash; , ad esempio, la convoluzione seguita dall'attivazione &mdash; può essere *fusa* insieme in un singolo metacomando. A causa di questi fattori, DirectML offre la possibilità di superare le prestazioni di un compute shader ottimizzato per la mano, scritto per l'esecuzione in un'ampia gamma di hardware.

I metacomandi fanno parte dell'API Direct3D 12, anche se sono vagamente collegati. Un metacomando è identificato da un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)fisso, mentre quasi tutti gli altri elementi (dal comportamento e dalla semantica alla firma e al nome) non fanno parte dell'API Direct3D 12. Viene invece specificato un metacommand tra l'autore e il driver che lo implementa. In questo caso, l'autore è DirectML. I metacomandi sono primitivi Direct3D 12 (proprio come Draw e spedites), quindi possono essere registrati in un elenco di comandi e pianificati per l'esecuzione insieme.

DirectML accelera i carichi di lavoro di Machine Learning usando un'intera suite di metacomandi di machine learning. Di conseguenza, non è necessario scrivere percorsi di codice specifici del fornitore per ottenere l'accelerazione hardware per l'inferenza. Se l'esecuzione avviene su un chip accelerato per intelligenza artificiale, DirectML usa tale hardware per accelerare significativamente le operazioni, ad esempio la convoluzione. È possibile usare lo stesso codice scritto, senza modificarlo, eseguirlo su un chip non accelerato dall'intelligenza artificiale (probabilmente la GPU integrata nel computer portatile) e ottenere comunque un'accelerazione hardware GPU eccezionale. Se non è disponibile alcuna GPU, DirectML esegue il fallback alla CPU.
