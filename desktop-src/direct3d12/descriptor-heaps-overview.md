---
title: Cenni preliminari sugli heap di descrittori
description: Gli heap del descrittore contengono molti tipi di oggetto che non fanno parte di un oggetto di stato della pipeline (PSO), ad esempio viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costante (CBVs) e Samplers.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bf720ebb71d016457fa4383a8d33aa62e2eee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104838"
---
# <a name="descriptor-heaps-overview"></a>Cenni preliminari sugli heap di descrittori

Gli heap del descrittore contengono molti tipi di oggetto che non fanno parte di un oggetto di stato della pipeline (PSO), ad esempio viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costante (CBVs) e Samplers.

-   [Scopo degli heap dei descrittori](#the-purpose-of-descriptor-heaps)
-   [Sincronizzazione](#synchronization)
-   [Associazione](#binding)
-   [Spostamento di heap](#switching-heaps)
-   [Bundle](#bundles)
-   [Gestione](#management)
-   [Argomenti correlati](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>Scopo degli heap dei descrittori

Lo scopo principale di un heap dei descrittori è includere la maggior parte dell'allocazione di memoria necessaria per archiviare le specifiche del descrittore dei tipi di oggetto a cui fanno riferimento gli shader per il maggior numero possibile di una finestra di rendering (idealmente un intero frame di rendering o più). Se un'applicazione sta cambiando le trame che la pipeline rileva rapidamente dall'API, è necessario che nell'heap del descrittore vengano definite le tabelle dei descrittori in tempo reale per ogni set di stato necessario. L'applicazione può scegliere di riutilizzare le definizioni se le risorse vengono riutilizzate in un altro oggetto, ad esempio, o semplicemente di assegnare lo spazio dell'heap in modo sequenziale durante la commutazione di diversi tipi di oggetto.

Gli heap dei descrittori consentono inoltre ai singoli componenti software di gestire l'archiviazione descrittore separatamente.

Tutti gli heap sono visibili alla CPU. L'applicazione può anche richiedere quali proprietà di accesso alla CPU un heap dei descrittori deve avere (se presente), ovvero scrivere combinate, scrivere di nuovo e così via. Le app possono creare tutti gli heap dei descrittori desiderati con qualsiasi proprietà desiderata. Le app hanno sempre la possibilità di creare heap del descrittore esclusivamente per finalità di staging che non sono vincolate e vengono copiati negli heap descrittore usati per il rendering in modo necessario.

Esistono alcune restrizioni per gli elementi che possono essere inseriti nello stesso heap del descrittore. Le voci CBV, UAV e SRV possono trovarsi nello stesso heap del descrittore. Tuttavia, le voci dei sampler non possono condividere un heap con le voci CBV, UAV o SRV. In genere, sono disponibili due insiemi di heap dei descrittori, uno per le risorse comuni e il secondo per i sampler.

L'uso degli heap dei descrittori di Direct3D 12 rispecchia la maggior parte dell'hardware GPU, che richiede che i descrittori siano attivi solo negli heap dei descrittori o semplicemente che siano necessari meno bit di indirizzamento se vengono usati questi heap. Direct3D 12 richiede l'uso di heap di descrittori. non è possibile inserire descrittori in qualsiasi punto della memoria.

Gli heap dei descrittori possono essere modificati immediatamente solo dalla CPU, ma non è possibile modificare un heap dei descrittori tramite la GPU.

## <a name="synchronization"></a>Sincronizzazione

Il contenuto dell'heap del descrittore può essere modificato prima, durante e dopo la registrazione degli elenchi di comandi che vi fanno riferimento. Tuttavia, i descrittori non possono essere modificati mentre un elenco di comandi inviato per l'esecuzione può fare riferimento a tale percorso, in quanto questo può richiamare un race condition.

## <a name="binding"></a>Binding

È possibile associare al massimo un heap combinato CBV/SRV/UAV e un heap campionatore alla volta. Questi heap sono condivisi tra le pipeline di calcolo e di grafica (descritte in PSO).

## <a name="switching-heaps"></a>Spostamento di heap

È accettabile che un'applicazione Commuti gli heap nello stesso elenco di comandi o in quelli diversi usando le API [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) e [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) . In alcuni componenti hardware può trattarsi di un'operazione costosa, che richiede la disattivazione di una GPU per lo scaricamento di tutte le operazioni che dipendono dall'heap del descrittore attualmente associato. Di conseguenza, se è necessario modificare gli heap del descrittore, le applicazioni devono provare a farlo quando il carico di lavoro della GPU è relativamente leggero, forse limitando le modifiche all'inizio di un elenco di comandi.

## <a name="bundles"></a>Bundle

Con Bundle è possibile eseguire una sola chiamata al metodo [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) e gli heap del descrittore impostati devono corrispondere esattamente a quelli dell'elenco di comandi che chiama il bundle. Se il bundle non modifica le tabelle dei descrittori, non è necessario impostare gli heap del descrittore.

Per un elenco di chiamate API che non possono essere usate con bundle, vedere [creazione e registrazione di elenchi di comandi e bundle](recording-command-lists-and-bundles.md).

## <a name="management"></a>Gestione

Per eseguire il rendering di tutti gli oggetti in una scena, saranno necessari molti descrittori ed è possibile seguire alcune strategie di gestione diverse.

La strategia più semplice consiste nel compilare un'area aggiornata dell'heap dei descrittori con tutti i requisiti per la chiamata di estrazione successiva. Quindi, appena prima di emettere la chiamata di progetto nell'elenco dei comandi, un puntatore alla tabella del descrittore verrebbe impostato sull'inizio della tabella appena popolata. Il lato positivo è che non è necessario registrare la posizione di un determinato descrittore nell'heap.

Lo svantaggio di questa strategia è costituito dal fatto che potrebbe esserci una grande ripetizione di descrittori nell'heap del descrittore, specialmente quando viene eseguito il rendering di una scena molto simile e lo spazio dell'heap del descrittore verrà utilizzato rapidamente. Gli heap dei descrittori separati per i quali viene eseguito il rendering sulla GPU e per quelli registrati dalla CPU possono essere probabilmente necessari per evitare conflitti. In alternativa, è possibile usare un sistema di suddivisione delle sottoallocazioni.

Inoltre, il sistema di base potrebbe essere ulteriormente ottimizzato con un utilizzo accurato di tabelle descrittore sovrapposte da una chiamata di creazione a quella successiva, in modo che vengano aggiunti solo i nuovi descrittori richiesti.

Una strategia più efficiente rispetto a quella di base consiste nel precompilare gli heap dei descrittori con i descrittori necessari per gli oggetti (o materiali) noti come parte della scena. L'idea è che è necessario solo impostare la tabella descrittore in fase di estrazione, perché l'heap del descrittore viene popolato in anticipo.

Una variante della strategia di pre-riempimento consiste nel considerare l'heap del descrittore come una grande matrice, che contiene tutti i descrittori richiesti in posizioni note fisse. Quindi la chiamata di progetto deve solo ricevere un set di costanti che sono gli indici nella matrice di in cui devono essere usati i descrittori.

Un'ulteriore ottimizzazione consiste nel garantire che le costanti radice e i descrittori radice contengano quelli che cambiano più di frequente, anziché inserire costanti nell'heap del descrittore. Per la maggior parte dell'hardware, si tratta di un modo efficiente per gestire le costanti.

In pratica, un motore di grafica può utilizzare una strategia diversa in situazioni diverse e combinare gli elementi di ogni strategia per soddisfare i requisiti di disegno specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 




