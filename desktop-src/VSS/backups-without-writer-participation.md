---
description: Quando un'operazione di backup VSS viene eseguita senza il coinvolgimento di un writer, la creazione della copia shadow può ancora verificarsi.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Backup senza partecipazione del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318907"
---
# <a name="backups-without-writer-participation"></a>Backup senza partecipazione del writer

Quando un'operazione di backup VSS viene eseguita senza il coinvolgimento di un writer, la creazione della copia shadow può ancora verificarsi.

Come indicato altrove (vedere [lo stato predefinito della copia shadow](shadow-copies-and-shadow-copy-sets.md)), il risultato di questo tipo di copia shadow è costituito da un volume che riflette lo stato di un disco al momento della copia shadow: i dati nel volume copiato shadow possono riflettere operazioni di I/o incomplete o parziali ed è descritto come in uno [*stato di arresto anomalo*](vssgloss-c.md)del sistema.

Esistono diverse situazioni in cui è necessario che un'applicazione di backup funzioni con i dati copiati shadow coerenti con l'arresto anomalo del sistema:

-   **I dati sono gestiti da applicazioni non compatibili con VSS**

    Quasi tutti i sistemi disporranno di alcune applicazioni, ad esempio editor di testo, lettori di posta elettronica, elaboratori di testi e così via, che non sono in grado di ignorare, quindi è sempre probabile che alcuni dati di una copia shadow debbano essere considerati in uno stato coerente con l'arresto anomalo.

    Questo tipo di dati non è in genere critico dal sistema o dal servizio, pertanto il backup non dovrebbe essere problematico o almeno non più problematico rispetto a un backup convenzionale.

    Come per i preparativi per i backup convenzionali, se possibile, gli operatori di backup devono tentare di sospendere o terminare tali applicazioni prima di avviare un processo di backup VSS.

-   **Sistema senza writer compatibili con VSS**

    Questa situazione può essere relativamente rara poiché la maggior parte dei sistemi di cui è possibile eseguire il backup da un'applicazione di backup VSS avrà una versione di Windows abilitata per VSS, che dovrebbe contenere writer.

    Tuttavia, in alcune circostanze potrebbe verificarsi questo problema, ad esempio se si esegue il backup di un sistema senza supporto VSS, ma il sistema usa un'appliance di rete abilitata per VSS per la relativa archiviazione.

    Sebbene il backup dello stato di un sistema da un'immagine coerente con l'arresto anomalo non sia ottimale, potrebbe essere sufficiente che un computer riavvii lo stato operativo. In molti casi, il computer ripristinerà le operazioni di I/O incomplete nei file System e funzionerà normalmente.

-   **Un richiedente che sceglie di non usare i writer di sistema**

    Questa circostanza si verifica se un richiedente ha scelto di non aggiungere componenti del writer o disabilitare tutti i writer.

    L'esecuzione di backup in questo modo è in genere sconsigliata. Sebbene il volume copiato dall'ombreggiatura per eseguire il backup potrebbe essere sufficiente per ripristinare un sistema in esecuzione, non è consigliabile. Infatti, dato che i writer in esecuzione nel sistema sono progettati con funzionalità per collaborare con VSS e copie shadow, il backup dei dati in questo modo potrebbe causare instabilità.

 

 



