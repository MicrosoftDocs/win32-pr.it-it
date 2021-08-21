---
description: È possibile usare COM+ Compensating Resource Manager (CRM) per integrare in modo semplice e rapido le risorse dell'applicazione con Microsoft Distributed Transaction Coordinator (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Concetti relativi alla compensazione Resource Manager COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b546f10e9a99f827c512e6dd7662ead05476774f7ff8dc32c40fa123b0ffe272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047629"
---
# <a name="com-compensating-resource-manager-concepts"></a>Concetti relativi alla compensazione Resource Manager COM+

È possibile usare COM+ Compensating Resource Manager (CRM) per integrare in modo semplice e rapido le risorse dell'applicazione con Microsoft Distributed Transaction Coordinator (DTC). Le risorse dell'applicazione possono votare sul risultato di una transazione e possono ricevere la notifica finale del risultato. Viene generato un log durevole in modo che le risorse dell'applicazione possano scrivere record che possono sopravvivere a errori e il CRM recupera questo file di log al riavvio dell'applicazione.

Un CRM è costituito dai due componenti seguenti:

-   Ruolo di lavoro CRM. Questo componente esegue il lavoro principale del CRM specifico e implementa un'interfaccia specifica per l'attività che deve eseguire. L'infrastruttura CRM fornisce un'interfaccia al ruolo di lavoro CRM tramite cui il ruolo di lavoro CRM può scrivere record in un file di log durevole su disco. Il ruolo di lavoro CRM deve scrivere record nel log e renderli durevoli prima di eseguire il proprio lavoro in modo che, in caso di arresto anomalo, il ripristino possa verificarsi correttamente. Il ruolo di lavoro CRM richiede sempre una transazione.
-   CRM Compensator. Questo componente viene creato dall'infrastruttura CRM al completamento della transazione. Implementa un'interfaccia definita tramite la quale l'infrastruttura CRM può passare le notifiche di completamento delle transazioni e i record di log scritti in precedenza dal ruolo di lavoro CRM.

Un CRM COM+ fornisce atomicità con notifiche transazionali e durabilità con il log CRM, ma non fornisce l'isolamento delle risorse. In un ambiente multithreading è responsabilità dello sviluppatore CRM assicurarsi che l'accesso alle risorse, da parte di più operatori CRM o applicazioni esterne, sia serializzato durante una transazione.

Dopo che la transazione ha superato la fase di preparazione, i processi di compensazione CRM e crm worker possono essere eseguiti contemporaneamente. È possibile che il componente CRM Worker di una nuova transazione diventi attivo mentre CRM Compensator di una transazione precedente sta ancora elaborando la transazione precedente.

Durante gli errori prima del ripristino dell'applicazione server CRM, una transazione interrotta deve essere considerata attiva e non completata. Non dovrebbe essere possibile che i processi esterni accedono alle risorse modificate da questa particolare transazione prima del ripristino del processo del server CRM.

Crm definisce tre tipi di interfaccia per le funzioni CRM di base:

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) viene implementato nel clerk CRM e viene usato dal ruolo di lavoro CRM per scrivere record di log nel log. Può essere usato anche dal compensatore CRM.
-   [**ICrmCompensator e**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) vengono implementati in CRM Compensator. Queste interfacce vengono usate per recapitare le notifiche dei risultati delle transazioni e i record di log associati al compensatore CRM. In genere, CRM Compensator implementa solo una di queste interfacce, a seconda che siano necessari record di log non strutturati o strutturati. *I record di log* strutturati sono quelli compilati come una raccolta di varianti e vengono in genere utilizzati da Microsoft Visual Basic. *I record di log non* strutturati sono solo un buffer di byte e vengono in genere utilizzati da Microsoft Visual C++. Un compensatore CRM può implementare entrambe le interfacce del compensatore. Tuttavia, per recapitare i record di log viene usato solo uno alla volta.
-   Le interfacce di monitoraggio COM+ CRM vengono usate per il monitoraggio dei CPM all'interno di una determinata applicazione server. Per informazioni dettagliate sulle interfacce di monitoraggio, vedere [COM+ CRM Monitoring Interfaces](com--crm-monitoring-interfaces.md).

Gli argomenti seguenti in questa sezione forniscono informazioni più dettagliate sul servizio COM+ CRM:

-   [Considerazioni sulla sicurezza di COM+ CRM](com--crm-security-considerations.md)
-   [Processo operativo COM+ CRM](com--crm-operating-process.md)
-   [Avvio e ripristino di COM+ CRM](com--crm-startup-and-recovery.md)
-   [Uso di COM+ CRM in un ambiente cluster](using-the-com--crm-in-a-cluster-environment.md)
-   [Gestione degli errori in COM+ CRM](error-handling-in-the-com--crm.md)
-   [Registro COM+ CRM Impostazioni](com--crm-registry-settings.md)
-   [Risoluzione dei problemi di COM+ CRM](troubleshooting-the-com--crm.md)
-   [Suggerimenti di progettazione per lo sviluppo di un CRM COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfacce di monitoraggio CRM COM+](com--crm-monitoring-interfaces.md)
-   [Interfacce COM+ CRM](com--crm-interfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[COM+ Compensating Resource Manager Tasks](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



