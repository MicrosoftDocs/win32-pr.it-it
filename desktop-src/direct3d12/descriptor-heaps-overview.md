---
title: Panoramica degli heap dei descrittori
description: Gli heap dei descrittori contengono molti tipi di oggetto che non fanno parte di un oggetto stato della pipeline (PSO), ad esempio viste di risorse shader(SPV), viste di accesso non ordinate (UAV), visualizzazioni buffer costanti (CBV) e campionatori.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d0017f10a6027fc7ce48618a9d28bd4e92262d83d0f3aa81cc0bc8d02b7edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124336"
---
# <a name="descriptor-heaps-overview"></a>Panoramica degli heap dei descrittori

Gli heap dei descrittori contengono molti tipi di oggetto che non fanno parte di un oggetto stato della pipeline (PSO), ad esempio viste di risorse shader(SPV), viste di accesso non ordinate (UAV), visualizzazioni buffer costanti (CBV) e campionatori.

-   [Scopo degli heap dei descrittori](#the-purpose-of-descriptor-heaps)
-   [Sincronizzazione](#synchronization)
-   [Binding](#binding)
-   [Passaggio da un heap all'altro](#switching-heaps)
-   [Pacchetti](#bundles)
-   [Gestione](#management)
-   [Argomenti correlati](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>Scopo degli heap dei descrittori

Lo scopo principale di un heap dei descrittori è quello di includere la maggior parte dell'allocazione di memoria necessaria per archiviare le specifiche del descrittore dei tipi di oggetto a cui fanno riferimento gli shader per il maggior numero possibile di finestre di rendering (idealmente un intero frame di rendering o più). Se un'applicazione cambia le trame che la pipeline vede rapidamente dall'API, deve essere presente spazio nell'heap dei descrittori per definire le tabelle dei descrittori in tempo reale per ogni set di stato necessario. L'applicazione può scegliere di riutilizzare le definizioni se le risorse vengono usate di nuovo in un altro oggetto, ad esempio, o semplicemente assegnare lo spazio dell'heap in modo sequenziale quando si passa da un tipo di oggetto all'altro.

Gli heap dei descrittori consentono inoltre ai singoli componenti software di gestire separatamente l'archiviazione dei descrittori.

Tutti gli heap sono visibili alla CPU. L'applicazione può anche richiedere quali proprietà di accesso alla CPU devono avere (se presenti) un heap descrittore: scrittura combinata, write back e così via. Le app possono creare tutti gli heap dei descrittori desiderati con le proprietà desiderate. Le app hanno sempre la possibilità di creare heap di descrittori esclusivamente per scopi di gestione temporanea di cui non è stato vincolato il training e di copiare negli heap dei descrittori usati per il rendering in base alle esigenze.

Esistono alcune restrizioni in cosa può andare nello stesso heap descrittore. Le voci CBV, UAV e SRV possono essere nello stesso heap descrittore. Tuttavia, le voci dei campionatori non possono condividere un heap con voci CBV, UAV o SRV. In genere, esistono due set di heap dei descrittori, uno per le risorse comuni e il secondo per i campionatori.

L'uso degli heap dei descrittori da parte di Direct3D 12 rispecchia le operazioni della maggior parte dell'hardware GPU, ovvero richiedere che i descrittori siano presenti solo negli heap dei descrittori o semplicemente che siano necessari meno bit di indirizzamento se vengono usati questi heap. Direct3D 12 richiede l'uso di heap dei descrittori. Non è possibile inserire i descrittori in un punto qualsiasi della memoria.

Gli heap dei descrittori possono essere modificati solo immediatamente dalla CPU, non è possibile modificare un heap descrittore dalla GPU.

## <a name="synchronization"></a>Sincronizzazione

Il contenuto dell'heap dei descrittori può essere modificato prima, durante e dopo la registrazione degli elenchi di comandi che fanno riferimento a esso. Tuttavia, i descrittori non possono essere modificati mentre un elenco di comandi inviato per l'esecuzione potrebbe fare riferimento a tale percorso, perché potrebbe richiamare un race condition.

## <a name="binding"></a>Binding

Al massimo un heap combinato CBV/SRV/UAV e un heap del campionatore possono essere associati in qualsiasi momento. Questi heap vengono condivisi tra le pipeline di grafica e di calcolo (descritte nei relativi oggetti PSO).

## <a name="switching-heaps"></a>Passaggio da un heap all'altro

È accettabile per un'applicazione cambiare heap all'interno dello stesso elenco di comandi o in uno diverso usando le API [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) e [**Reset.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) In alcuni componenti hardware può trattarsi di un'operazione dispendiosa, che richiede un blocco della GPU per scaricare tutto il lavoro che dipende dall'heap del descrittore attualmente associato. Di conseguenza, se è necessario modificare gli heap dei descrittori, le applicazioni devono provare a farlo quando il carico di lavoro della GPU è relativamente leggero, limitando ad esempio le modifiche all'inizio di un elenco di comandi.

## <a name="bundles"></a>Pacchetti

Con i bundle può essere presente una sola chiamata al metodo [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) e gli heap dei descrittori impostati devono corrispondere esattamente a quelli dell'elenco di comandi che chiama il bundle. Se il bundle non modifica le tabelle dei descrittori, non è necessario impostare gli heap dei descrittori.

Per un elenco di chiamate API che non possono essere usate con i bundle, vedere Creazione e registrazione di elenchi di [comandi e bundle.](recording-command-lists-and-bundles.md)

## <a name="management"></a>Gestione

Per eseguire il rendering di tutti gli oggetti in una scena, saranno necessari molti descrittori ed è possibile seguire alcune strategie di gestione diverse.

La strategia più semplice consiste nel riempire una nuova area dell'heap dei descrittori con tutti i requisiti per la chiamata di disegno successiva. Quindi, appena prima di eseguire la chiamata di disegno sull'elenco di comandi, un puntatore alla tabella dei descrittori viene impostato sull'inizio della tabella appena popolata. Lo svantaggio è che non è necessario registrare dove un determinato descrittore si trova nell'heap.

Lo svantaggio di questa strategia è che potrebbe essere presente una grande ripetizione di descrittori nell'heap dei descrittori, soprattutto quando viene eseguito il rendering di una scena molto simile e lo spazio dell'heap dei descrittori verrà usato rapidamente. Heap descrittori separati per quelli di cui viene eseguito il rendering nella GPU e per quelli registrati dalla CPU, probabilmente saranno necessari per evitare conflitti. In alternativa, è possibile usare un sistema di sottoallocazione.

Inoltre, il sistema di base può essere ulteriormente ottimizzato con un attento uso di tabelle descrittori sovrapposte da una chiamata di disegno alla successiva, in modo che siano aggiunti solo i nuovi descrittori necessari.

Una strategia più efficiente rispetto a quella di base consiste nel precompilare gli heap dei descrittori con i descrittori necessari per gli oggetti (o materiali) noti come parte della scena. In questo caso è necessario impostare la tabella dei descrittori solo in fase di disegno, perché l'heap dei descrittori viene popolato in anticipo.

Una variante della strategia di riempimento preliminare consiste nel considerare l'heap dei descrittori come una matrice di grandi dimensioni, contenente tutti i descrittori necessari in posizioni note fisse. La chiamata di disegno deve quindi ricevere solo un set di costanti che sono gli indici nella matrice di in cui devono essere usati i descrittori.

Un'ulteriore ottimizzazione è garantire che le costanti radice e i descrittori radice contengano quelle che cambiano più frequentemente, anziché inserire costanti nell'heap dei descrittori. Per la maggior parte dell'hardware si tratta di un modo efficiente per gestire le costanti.

In pratica, un motore di grafica potrebbe usare una strategia diversa in situazioni diverse e combinare gli elementi di ogni strategia in base ai requisiti di disegno specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 




