---
description: Processo operativo COM+ CRM
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Processo operativo COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39dba3dedcbdefebe0f62144547ebb6985fa51f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878281"
---
# <a name="com-crm-operating-process"></a>Processo operativo COM+ CRM

In un'operazione normale, un componente dell'applicazione in esecuzione in un processo di applicazione server utilizzerebbe un CRM COM+ creando un ruolo di lavoro CRM. Il ruolo di lavoro CRM implementa un'interfaccia COM specifica dell'attività progettata per l'esecuzione. Il componente dell'applicazione deve essere in esecuzione in una transazione, in modo che il processo di lavoro CRM erediti la transazione del componente dell'applicazione. I thread di lavoro CRM richiedono sempre una transazione.

Per accedere a COM+ CRM, il ruolo di lavoro CRM ottiene innanzitutto l'interfaccia [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) , che consente al ruolo di lavoro CRM di scrivere record nel log durevole. Il ruolo di lavoro CRM ottiene questa interfaccia creando un componente Clerk CRM.

Il ruolo di lavoro CRM deve quindi indicare al Clerk CRM il nome del compensatore CRM che vuole usare. Questa operazione viene eseguita chiamando il metodo [**ICrmLogControl:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) . Dopo la chiamata a questo metodo, il compensatore CRM viene creato dall'infrastruttura CRM quando la transazione viene completata.

Dopo aver registrato il compensatore CRM, il ruolo di lavoro CRM può scrivere record nel log CRM usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Il ruolo di lavoro CRM deve *scrivere in anticipo*; ovvero, deve scrivere un record nel log che descrive un'azione prima di eseguire effettivamente l'azione, nel caso in cui si verifichi un arresto anomalo immediatamente dopo aver completato l'azione. Senza questi record di log write-ahead, non esiste alcun modo per correggere l'azione.

Inoltre, write-ahead significa che il compensatore CRM, che è il componente che riceve i record del log al recupero, deve gestire il caso in cui sono stati scritti i record del log, ma l'azione non è stata effettivamente eseguita. Le azioni eseguite dal compensatore CRM devono essere *idempotente*; ovvero, devono essere in grado di essere eseguite più di una volta, ma dovrebbero dare lo stesso risultato. Ad esempio, l'impostazione di un saldo del conto sul valore $100 è un'azione idempotente. non è possibile aggiungere $100 al saldo del conto.

L'interfaccia [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) fornisce i due metodi seguenti per la scrittura dei record di log:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) viene utilizzata per la scrittura di un record di log strutturato compilato come una raccolta di varianti. Viene utilizzato principalmente per lo sviluppo di dispongono in Microsoft Visual Basic.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) viene utilizzato per la scrittura di un record di log non strutturato come BLOB di byte. Viene utilizzato principalmente per lo sviluppo di dispongono in Microsoft Visual C++. Poiché le strutture di record in C sono spesso costituite da un set di intestazioni e campi che possono essere dispersi in memoria, il metodo **WriteLogRecord** implementa una funzionalità di raccolta che riduce la copia dei dati.

> [!Note]  
> I tipi di puntatore utente non devono essere presenti all'interno di strutture di dati in un record di log. I puntatori non sono più validi durante la fase di recupero perché il compensatore CRM viene eseguito in un processo diverso rispetto a quello del ruolo di lavoro CRM che ha scritto il record di log. L'inclusione di tipi di puntatore in un record di log potrebbe causare l'arresto anomalo o il danneggiamento di un'applicazione durante il ripristino

 

Entrambi questi metodi di scrittura scrivono un record di log su disco, ma non garantiscono la durabilità del record. Sebbene le scritture lazy si accumulino prima di forzare il disco in modo da poter migliorare le prestazioni, è possibile usare il metodo [**ICrmLogControl:: ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) per garantire che tutte le scritture eseguite dal CRM siano durevoli sul disco, operazione importante per il ripristino degli errori.

Quando il ruolo di lavoro CRM viene eseguito con le azioni e ha terminato di scrivere e forzare i record nel log, deve rilasciare [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Quando la transazione viene completata (in genere a causa del componente dell'applicazione che chiama [**Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)), l'infrastruttura CRM crea il componente compensatore CRM, che implementa l'interfaccia [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) o l'interfaccia [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) . Queste interfacce vengono usate per passare i record non strutturati (Visual C++) o strutturati (Visual Basic) al compensatore CRM insieme alle notifiche relative al risultato della transazione.

Il compensatore CRM riceve prima una notifica della fase di preparazione del completamento della transazione e può votare la richiesta di preparazione, sì o no. Se il compensatore CRM ha votato, non riceve altre notifiche di interruzione. Se vota sì alla richiesta di preparazione, riceve le notifiche di commit o di interruzione. In caso di interruzione di un client, non vengono ricevute notifiche di preparazione, ma solo le notifiche di interruzione. Il compensatore CRM deve essere pronto a gestire tutti questi casi e deve anche gestire il caso in cui nessun record di log è stato scritto correttamente dal ruolo di lavoro CRM. Il compensatore CRM non deve presupporre che la stessa istanza del compensatore CRM riceva le notifiche fase 1 (preparazione) e fase 2 (commit o Interrompi), in quanto potrebbero essere interrotte dal ripristino.

In genere, un compensatore CRM usa la notifica di interruzione per invertire l'azione eseguita dal ruolo di lavoro CRM. Il ruolo di lavoro CRM potrebbe lasciare uno stato disponibile se è necessario invertire l'azione. Tale stato potrebbe essere completamente contenuto nei record di log. in caso contrario, il compensatore CRM deve pulire tale stato se la transazione viene sottoposto a commit. Questo è il motivo per cui il compensatore CRM riceve la notifica di commit. Il compensatore CRM non viene eseguito in una transazione DTC.

Il compensatore CRM può registrare nuovi record se necessario usando [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol), che riceve come viene creato. Il ruolo di lavoro CRM e il compensatore CRM possono anche dimenticare l'ultimo record di log scritto, che potrebbe essere necessario per evitare il ripristino non necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Avvio e ripristino di COM+ CRM](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



