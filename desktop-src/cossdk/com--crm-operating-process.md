---
description: Processo operativo CRM COM+
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Processo operativo CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308130"
---
# <a name="com-crm-operating-process"></a>Processo operativo CRM COM+

In condizioni normali, un componente dell'applicazione in esecuzione in un processo dell'applicazione server usa un CRM COM+ creando un ruolo di lavoro CRM. Il ruolo di lavoro CRM implementa un'interfaccia COM specifica per l'attività che è progettata per eseguire. Il componente dell'applicazione deve essere in esecuzione in una transazione in modo che il ruolo di lavoro CRM erediti la transazione del componente dell'applicazione. I crm worker richiedono sempre una transazione.

Per accedere a COM+ CRM, il ruolo di lavoro CRM ottiene innanzitutto [**l'interfaccia ICrmLogControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) che consente al ruolo di lavoro CRM di scrivere record nel log durevole. Il ruolo di lavoro CRM ottiene questa interfaccia creando un componente clerk CRM.

Successivamente, il ruolo di lavoro CRM deve indicare al clerk CRM il nome della classe CRM Compensator che vuole usare. A tale scopo, chiama il [**metodo ICrmLogControl::RegisterCompensator.**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) Dopo la chiamata a questo metodo, crm Compensator viene creato dall'infrastruttura CRM al termine della transazione.

Dopo che il ruolo di lavoro CRM ha registrato crm Compensator, può scrivere record nel log CRM [**usando ICrmLogControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) Il ruolo di lavoro CRM deve *scrivere in anticipo;* ciò significa che deve scrivere un record nel log che descrive un'azione prima di eseguire effettivamente l'azione, nel caso in cui si verifichi un arresto anomalo immediatamente dopo il completamento dell'azione. Senza questi record di log write-ahead, non è possibile correggere l'azione.

Inoltre, write-ahead significa che CRM Compensator, ovvero il componente che riceve i record di log al ripristino, deve gestire il caso in cui i record di log sono stati scritti, ma l'azione non è stata eseguita. Le azioni di CRM Compensator devono essere *idempotenti.* ciò significa che devono essere in grado di essere eseguiti più volte, ma dovrebbero portare allo stesso risultato. Ad esempio, l'impostazione di un saldo del conto sul valore di $ 100 è un'azione idempotente. l'aggiunta di $ 100 al saldo del conto non lo è.

[**L'interfaccia ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) fornisce i due metodi seguenti per la scrittura dei record di log:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) viene usato per scrivere un record di log strutturato creato come raccolta di varianti. È destinato principalmente allo sviluppo di CRM in Microsoft Visual Basic.
-   [**WriteLogRecord viene**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) usato per scrivere un record di log non strutturato come BLOB di byte. È destinato principalmente allo sviluppo di CRM in Microsoft Visual C++. Poiché le strutture di record in C sono spesso rappresentate da un set di intestazioni e campi che possono essere sparsi in memoria, il **metodo WriteLogRecord** implementa una funzionalità di raccolta che riduce la copia dei dati.

> [!Note]  
> Non è consigliabile utilizzare tipi puntatore all'interno di strutture di dati in un record di log. I puntatori non sono più validi durante la fase di ripristino perché CRM Compensator viene eseguito in un processo diverso da quello del ruolo di lavoro CRM che ha scritto il record di log. L'inclusione dei tipi di puntatore in un record di log può causare l'arresto anomalo o il danneggiamento di un'applicazione durante il ripristino.

 

Entrambi questi metodi di scrittura scrivono un record di log su disco, ma non garantiscono la durabilità del record. Anche se consentire l'accumulo di scritture lazy prima di forzare il disco può migliorare le prestazioni, è possibile usare il metodo [**ICrmLogControl::ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) per garantire che tutte le scritture eseguite da CRM siano durevoli sul disco, operazione importante per il ripristino degli errori.

Quando il ruolo di lavoro CRM ha completato le azioni e ha terminato di scrivere e forzare i record nel log, deve rilasciare [**ICrmLogControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) Quando la transazione viene completata (in genere a causa del componente dell'applicazione che chiama [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**SetAbort),**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)l'infrastruttura CRM crea il componente CRM Compensator, che implementa l'interfaccia [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) o [**L'interfaccia ICrmCompensatorVariants.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) Queste interfacce vengono usate per passare i record non strutturati (Visual C++) o strutturati (Visual Basic) a CRM Compensator insieme alle notifiche dei risultati della transazione.

Crm Compensator viene prima notificato della fase di preparazione del completamento della transazione e può votare sì o no alla richiesta di preparazione. Se CRM Compensator vota no, non riceve altre notifiche di interruzione. Se vota sì alla richiesta di preparazione, riceve le notifiche di commit o di interruzione. In caso di interruzione del client, non vengono ricevute notifiche di preparazione, ma solo notifiche di interruzione. Crm Compensator deve essere preparato per gestire tutti questi casi e deve anche gestire il caso in cui il ruolo di lavoro CRM non ha scritto correttamente alcun record di log. Crm Compensator non deve presupporre che la stessa istanza di CRM Compensator riceva sia le notifiche della fase 1 (preparazione) che della fase 2 (commit o interruzione), perché potrebbero essere interrotte dal ripristino.

In genere, crm Compensator usa la notifica di interruzione per invertire l'azione eseguita dal ruolo di lavoro CRM. Il ruolo di lavoro CRM potrebbe lasciare disponibile uno stato nel caso in cui sia necessario annullare l'azione. Tale stato potrebbe essere completamente contenuto nei record di log e, in caso contrario, crm Compensator deve pulire tale stato se la transazione esegue il commit. Questo è il motivo per cui CRM Compensator riceve la notifica di commit. Crm Compensator non viene eseguito in una transazione DTC.

Crm Compensator può registrare nuovi record, se necessario, [**usando ICrmLogControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)che riceve durante la creazione. Sia il ruolo di lavoro CRM che CRM Compensator possono anche dimenticare l'ultimo record di log scritto, che potrebbe essere necessario per evitare un ripristino non necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Avvio e ripristino di COM+ CRM](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



