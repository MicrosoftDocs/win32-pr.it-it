---
description: È possibile utilizzare il Gestione risorse di compensazione COM+ (CRM) per integrare in modo semplice e rapido le risorse dell'applicazione con le transazioni Microsoft Distributed Transaction Coordinator (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Concetti Gestione risorse di compensazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966111"
---
# <a name="com-compensating-resource-manager-concepts"></a>Concetti Gestione risorse di compensazione COM+

È possibile utilizzare il Gestione risorse di compensazione COM+ (CRM) per integrare in modo semplice e rapido le risorse dell'applicazione con le transazioni Microsoft Distributed Transaction Coordinator (DTC). Le risorse dell'applicazione possono votare il risultato di una transazione e possono ricevere una notifica finale del suo esito. Viene generato un log durevole in modo che le risorse dell'applicazione possano scrivere record che sopravvivono a errori e il CRM ripristina il file di log quando l'applicazione viene riavviata.

Un CRM è costituito dai due componenti seguenti:

-   Ruolo di lavoro CRM. Questo componente esegue il lavoro principale del CRM specifico e implementa un'interfaccia specifica per l'attività da eseguire. L'infrastruttura CRM fornisce un'interfaccia per il ruolo di lavoro CRM tramite il quale il ruolo di lavoro CRM può scrivere record in un file di log durevole su disco. Il ruolo di lavoro CRM deve scrivere record nel log e renderli durevoli prima di eseguire il proprio lavoro in modo che, se si verifica un arresto anomalo, il ripristino possa essere eseguito correttamente. Il ruolo di lavoro CRM richiede sempre una transazione.
-   Compensatore CRM. Questo componente viene creato dall'infrastruttura CRM al completamento della transazione. Implementa un'interfaccia definita mediante la quale l'infrastruttura CRM può superare le notifiche di completamento delle transazioni e i record di log scritti in precedenza dal ruolo di lavoro CRM.

Un CRM COM+ fornisce l'atomicità con le notifiche transazionali e la durabilità con il log CRM, ma non fornisce l'isolamento delle risorse. In un ambiente con multithreading, è responsabilità dello sviluppatore di CRM garantire che l'accesso alle risorse, da più ruoli di lavoro CRM o da applicazioni esterne, venga serializzato in una transazione.

Dopo che la transazione ha superato la fase di preparazione, è possibile eseguire simultaneamente il compensatore CRM e i ruoli di lavoro CRM. È possibile che il componente Worker CRM di una nuova transazione diventi attivo mentre il compensatore CRM di una transazione precedente sta ancora elaborando la transazione precedente.

Durante gli errori prima del ripristino dell'applicazione server CRM, una transazione interrotta dovrebbe essere considerata attiva e non completata. Non dovrebbe essere possibile per i processi esterni accedere alle risorse che sono state modificate da questa particolare transazione prima del ripristino del processo del server CRM.

Il CRM definisce tre tipi di interfaccia per le funzioni CRM di base:

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) viene implementato nel Clerk CRM e viene usato dal ruolo di lavoro CRM per scrivere record di log nel log. Può anche essere usato dal compensatore CRM.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) e [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) sono implementati nella classe Compensator CRM. Queste interfacce vengono utilizzate per recapitare le notifiche dei risultati delle transazioni e i record di log associati al compensatore CRM. Il compensatore CRM, in genere, implementa solo una di queste interfacce, a seconda che siano necessari record di log non strutturati o strutturati. I *record di log strutturati* sono quelli compilati come una raccolta di varianti e vengono in genere utilizzati da Microsoft Visual Basic. I *record di log non strutturati* sono solo un buffer di byte e vengono in genere utilizzati da Microsoft Visual C++. Un compensatore CRM può implementare entrambe le interfacce del compensatore; Tuttavia, per recapitare i record di log viene usato solo uno alla volta.
-   Le interfacce di monitoraggio di COM+ CRM vengono utilizzate per il monitoraggio dei dispongono all'interno di una particolare applicazione server. Per informazioni dettagliate sulle interfacce di monitoraggio, vedere [interfacce di monitoraggio com+ CRM](com--crm-monitoring-interfaces.md).

Negli argomenti seguenti di questa sezione vengono forniti ulteriori dettagli sul servizio COM+ CRM:

-   [Considerazioni sulla sicurezza di COM+ CRM](com--crm-security-considerations.md)
-   [Processo operativo COM+ CRM](com--crm-operating-process.md)
-   [Avvio e ripristino di COM+ CRM](com--crm-startup-and-recovery.md)
-   [Utilizzo di COM+ CRM in un ambiente cluster](using-the-com--crm-in-a-cluster-environment.md)
-   [Gestione degli errori in COM+ CRM](error-handling-in-the-com--crm.md)
-   [Impostazioni del registro di sistema COM+ CRM](com--crm-registry-settings.md)
-   [Risoluzione dei problemi relativi a COM+ CRM](troubleshooting-the-com--crm.md)
-   [Suggerimenti di progettazione per lo sviluppo di un CRM COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfacce di monitoraggio COM+ CRM](com--crm-monitoring-interfaces.md)
-   [Interfacce COM+ CRM](com--crm-interfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di Gestione risorse di compensazione COM+](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



