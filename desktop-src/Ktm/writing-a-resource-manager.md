---
description: Se si sta scrivendo un servizio o un componente ed è necessario usare i servizi transazionali o se è necessario monitorare lo stato di una transazione kernel, è necessario creare un gestore di risorse (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Scrittura di un Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311125"
---
# <a name="writing-a-resource-manager"></a>Scrittura di un Gestione risorse

Se si sta scrivendo un servizio o un componente ed è necessario usare i servizi transazionali o se è necessario monitorare lo stato di una transazione kernel, è necessario creare un gestore di risorse (RM).

Per scrivere un gestore di risorse, è necessario creare più oggetti kernel. Gli oggetti utilizzati da un RM sono:

-   Oggetti di gestione transazioni (TM)
-   Oggetti Gestione risorse
-   Oggetti di integrazione

Per prima cosa, creare un oggetto TM. Esistono due tipi di TMs:

-   Volatile: le TMs non dispongono di un log e non possono recuperare il proprio stato
-   Durevole: le TM hanno un log

Per creare una TM durevole, è necessario creare un log CLFS e chiamare [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o fare in modo che KTM lo crei per l'utente. Dopo la creazione di una TM durevole, è necessario innanzitutto ripristinare la TM chiamando [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Una volta recuperato, il TM sarà disponibile per l'uso.

Se è stata ripristinata una TM esistente, tutte le RMs associate a questa TM inizieranno a ricevere i messaggi di ripristino. Per ulteriori informazioni, vedere [elaborazione del ripristino](recovery-processing.md).

Successivamente, creare un gestore di risorse chiamando [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con l'handle TM. Il RM può essere volatile o durevole. Con RMs durevole è possibile usare solo TMs durevoli.

Quando si lavora in modo transazionale, si integra la transazione chiamando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e specificando quali notifiche ricevere.

**Nota**  È possibile iniziare a ricevere le notifiche prima del completamento della chiamata a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .

Quando si riceve una notifica, chiamare la funzione "completa \* " appropriata quando viene completata qualsiasi lavoro associato all'elaborazione della notifica. Le funzioni complete sono:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Se in qualsiasi momento un gestore di risorse non è in grado di completare il lavoro della transazione o se continuare, il rendering dell'applicazione non è in grado di annullare le operazioni eseguite all'interno della transazione, è necessario eseguire il rollback della transazione chiamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



