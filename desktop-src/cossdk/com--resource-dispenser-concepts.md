---
description: I componenti dell'applicazione usano il dispenser di risorse COM+ per accedere e gestire informazioni sullo stato condivise e non durevoli, ad esempio le connessioni tra i componenti e un gestore di risorse specifico.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Concetti relativi al dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748066"
---
# <a name="com-resource-dispenser-concepts"></a>Concetti relativi al dispenser di risorse COM+

I componenti dell'applicazione usano il dispenser di risorse COM+ per accedere e gestire informazioni sullo stato condivise e non durevoli, ad esempio le connessioni tra i componenti e un gestore di risorse specifico. In fase di esecuzione, i pool dinamici di risorse, ad esempio le connessioni di database, le connessioni di rete, le connessioni a code, thread, oggetti e blocchi di memoria, vengono resi disponibili per il dispenser di risorse. Il processo dell'applicazione consente di ottenere prestazioni elevate utilizzando un numero minimo di risorse utilizzate di frequente. Il dispenser di risorse può anche automatizzare le transazioni e il recupero. Per ulteriori informazioni su questa funzionalità, vedere [recupero automatico delle risorse](automatic-resource-reclamation.md) .

> [!Note]  
> Una *risorsa* è un elemento creato da un dispenser di risorse. Una connessione a un gestore di risorse, ad esempio, è una risorsa comune. Le risorse si trovano nella memoria del dispenser di risorse e non vengono mai copiate nel gestore di dispenser. Una risorsa è nota solo da un handle opaco (**da un Resid**) e può o non essere in grado di eseguire transazioni. Sebbene le risorse gestite siano spesso connessioni a un componente che gestisce uno stato durevole, le connessioni stesse non sono durevoli. Un dispenser di risorse usa spesso un gestore di risorse correlato per mantenere lo stato durevole.

 

In architettura, il sistema di dispenser di risorse COM+ è costituito da distributori di risorse e da un responsabile del dispenser. I distributori di risorse sono componenti forniti dall'utente che forniscono applicazioni con interfacce semplici per le risorse condivise. Il gestore di dispenser è un componente fornito da COM+ che coordina le attività dei diversi dispenser di risorse.

Un dispenser di risorse è un componente libreria a collegamento dinamico (DLL) che fornisce almeno due interfacce. Il primo, [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver), fornisce al responsabile del dispenser le informazioni di base su come creare, eliminare e integrare le risorse gestite. Il secondo è esposto alle applicazioni e può essere un'interfaccia COM o un set di interfacce oppure può essere un Application Programming Interface (API) a cui un componente è collegato tramite una libreria di importazione. Un'applicazione può chiamare qualsiasi dispenser di risorse, che a sua volta può offrire qualsiasi API all'applicazione. Se il dispenser di risorse è un componente di automazione, è possibile accedervi da Microsoft Visual Basic. Viene creata un'istanza di un dispenser di risorse quando si fa riferimento a un componente dell'applicazione.

Il gestore di dispenser fornito da COM+ tiene traccia dei distributori di risorse e delle coordinate tra di essi. Implementa due interfacce: [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) e [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). i dispenser di risorse si registrano usando l'interfaccia **IDispenserManager** . Il gestore del dispenser fornisce quindi un puntatore a un **IHolder** che usa per notificare al responsabile del dispenser le proprie attività.

Un dispenser di risorse transazionali deve essere integrato in una transazione Distributed Transaction Coordinator (DTC). Ciò implica l'uso di un gestore di risorse interno o esterno (per il dispenser di risorse), che è conforme alle transazioni OLE.

> [!Note]  
> Nel modello di programmazione COM+ sono incluse *transazioni dichiarative*, che consentono di proteggere il lavoro eseguito da un oggetto applicazione durante la relativa durata. Quando un oggetto applicazione usa un dispenser di risorse COM+, il lavoro che esegue è automaticamente transazionale. ovvero, il componente non deve dichiarare in modo esplicito le transazioni. Queste transazioni sono definite nella specifica delle transazioni OLE, implementate dal DTC e avviate per conto dell'oggetto applicazione da COM+. Per ulteriori informazioni, vedere la Guida allo sviluppo di DTC.

 

Le risorse non devono essere transazionali. Un dispenser di risorse che consente di creare un pool di risorse non transazionali può comunque ottenere prestazioni elevate consentendo agli oggetti dell'applicazione di accedere a un pool condiviso di queste risorse. Questo tipo di dispenser di risorse restituisce \_ false dal metodo [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) , il che significa che il dispenser di risorse non ha integrato la risorsa perché la risorsa non è transazionale.

Il dispenser di risorse può anche funzionare indipendentemente da COM+, fornendo solo le funzionalità di pooling delle risorse. Se, ad esempio, un dispenser di risorse espone un'API, ad esempio ODBC, il dispenser di risorse potrebbe essere una DLL a cui l'applicazione accede tramite una libreria di importazione (oppure usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ). Un dispenser di risorse può anche essere un componente COM a cui un'applicazione accede chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Senza COM+, il metodo [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) di un dispenser di risorse non può mai essere chiamato perché il gestore del dispenser non conosce la transazione del componente corrente.

All'avvio, la DLL di un dispenser di risorse deve registrarsi con il gestore dispenser. Il responsabile del dispenser è il dirigente di controllo che gestisce il caricamento e lo scaricamento di dispenser di risorse, fornisce il contesto COM+ e controlla la gestione delle statistiche di inventario. Per ulteriori informazioni, vedere [com+ dispenser Manager](com--dispenser-manager.md). Il dispenser di risorse chiama prima la funzione [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) e quindi chiama il metodo [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) , passando il puntatore [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) che il dispenser di risorse implementa. Questa chiamata restituisce un riferimento a [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder).

Per arrestare, un dispenser di risorse chiama [**IHolder:: Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close). Per garantire l'arresto di un pacchetto pulito, un dispenser di risorse deve essere in grado di gestire la situazione in cui le chiamate continuano a provenire dagli oggetti business dopo che COM+ ha richiesto l'arresto del dispenser.

Negli argomenti seguenti di questa sezione vengono fornite informazioni più dettagliate sul servizio di dispenser di risorse COM+:

-   [Gestore di distribuzioni COM+](com--dispenser-manager.md)
-   [Tipi di thread del dispenser di risorse COM+](com--resource-dispenser-thread-types.md)
-   [Stati risorse in pool disponibili per il dispenser di risorse COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Integrazione di una risorsa in una transazione](enlisting-a-resource-in-a-transaction.md)
-   [Processo di allocazione delle risorse del dispenser di risorse](resource-dispenser-resource-allocation-process.md)
-   [Rilevamento di risorse non allocate](tracking-non-allocated-resources.md)
-   [Recupero automatico delle risorse](automatic-resource-reclamation.md)
-   [Tipi utilizzati nelle interfacce del dispenser di risorse COM+](types-used-in-com--resource-dispenser-interfaces.md)
-   [Interfacce del dispenser di risorse COM+](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività del dispenser di risorse COM+](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
