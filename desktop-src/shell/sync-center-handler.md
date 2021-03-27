---
description: Questo argomento fornisce un'analisi dettagliata dei requisiti per la compilazione di un file DLL che implementa un gestore da usare con il Centro sincronizzazione. Queste informazioni sono valide a partire da Windows Vista.
title: Sviluppo di un gestore del Centro sincronizzazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979799"
---
# <a name="developing-a-windows-sync-center-handler"></a>Sviluppo di un gestore del Centro sincronizzazione Windows

Questo argomento fornisce un'analisi dettagliata dei requisiti per la compilazione di un file DLL che implementa un gestore da usare con il Centro sincronizzazione. Queste informazioni sono valide a partire da Windows Vista.

-   [Esperienza di sincronizzazione di Windows prima di vista](#the-windows-synchronization-experience-before-vista)
-   [API del Centro sincronizzazione](#sync-center-apis)
    -   [Interfacce essenziali](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>Esperienza di sincronizzazione di Windows prima di vista

Windows XP ha fornito una [Gestione sincronizzazione](syncmgr-start-page.md) (mobsync.exe). Molti dispositivi, ad esempio lettori MP3, telefoni cellulari e fotocamere, forniscono anche le proprie interfacce di sincronizzazione anziché usare Gestione sincronizzazione. Ciò ha comportato un'esperienza utente non coerente e non centralizzata.

La nuova funzionalità del Centro sincronizzazione fornita in Windows Vista presenta diversi vantaggi rispetto alla gestione della sincronizzazione precedente.

-   Maggiore individuabilità
-   Minore necessità di azione diretta dell'utente
-   Non blocca altre operazioni
-   Migliore visualizzazione dello stato di avanzamento della sincronizzazione
-   Modello di sviluppo più semplice da comprendere

## <a name="sync-center-apis"></a>API del Centro sincronizzazione

Il Centro sincronizzazione comunica con i gestori tramite una serie di interfacce di Component Object Model (COM). Non tutte queste interfacce sono necessarie per implementare un gestore del Centro sincronizzazione. Questo argomento è stato suddiviso in due sezioni. La prima sezione illustra le interfacce COM essenziali che ogni gestore deve supportare e la seconda sezione esamina le interfacce COM facoltative ed esamina i motivi che un gestore li supporterà.

-   [Interfacce essenziali](#essential-interfaces)

### <a name="essential-interfaces"></a>Interfacce essenziali

Tutti i gestori del Centro sincronizzazione devono supportare le interfacce seguenti:

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) vengono usati per descrivere un singolo elemento di sincronizzazione che interessano la sincronizzazione con il centro di sincronizzazione. Un elemento di sincronizzazione rappresenta in genere un particolare tipo di dati, ad esempio immagini, o una particolare posizione di dati.

Gli elementi di sincronizzazione che rappresentano percorsi di dati diversi consentono sincronizzazioni molto specifiche. La granularità della posizione spetta all'autore del gestore, ma è necessario prestare attenzione alla progettazione. Se sono presenti troppi elementi di sincronizzazione (percorsi), l'utente è limitato alla possibilità di sincronizzare solo determinati dati. All'altro estremo, una granularità eccessiva può diventare non gestibile.

Se un gestore supporta più di un tipo di dati o più percorsi di dati, deve supportare più di un oggetto di sincronizzazione elemento. Un esempio può essere un PDA (Personal Data Assistant) che consente all'utente di sincronizzare contatti, elementi del calendario e documenti. Questi tre tipi di dati devono essere rappresentati da tre oggetti univoci, ciascuno dei quali espone le interfacce [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) .

L'interfaccia [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) fornisce un meccanismo per enumerare gli elementi di sincronizzazione di un gestore. Per recuperare l'enumeratore, il Centro sincronizzazione chiama il metodo [**ISyncMgrSyncItemContainer:: GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) esposto dal gestore. [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) contiene anche altri due metodi che possono essere usati dal Centro sincronizzazione per recuperare le informazioni sugli elementi di sincronizzazione del gestore:

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) restituisce un elemento di sincronizzazione specifico.
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) restituisce il numero di elementi di sincronizzazione supportati dal gestore.

[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) e [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) vengono usati per descrivere le proprietà del gestore e avviare la sincronizzazione effettiva. [**ISyncMgrHandler:: Synchronize**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) è il punto in cui il codice del gestore esegue la sincronizzazione e fornisce feedback sullo stato di avanzamento e sui problemi che si verificano.

Molti metodi di interfaccia non devono essere completamente implementati. Il Centro sincronizzazione fornisce una certa quantità di informazioni predefinite. Le interfacce consentono a un gestore di eseguire l'override di queste informazioni e fornire informazioni personalizzate da visualizzare, se necessario.

 

 



