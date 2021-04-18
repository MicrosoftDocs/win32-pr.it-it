---
description: Il modello di sicurezza di Windows consente ai chiamanti di gestione transazioni kernel di controllare l'accesso agli oggetti Transaction, gestione transazioni, Resource Manager e integrazione.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Diritti di accesso e sicurezza di KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317137"
---
# <a name="ktm-security-and-access-rights"></a>Diritti di accesso e sicurezza di KTM

Il modello di sicurezza di Windows consente ai chiamanti di gestione transazioni kernel di controllare l'accesso agli oggetti Transaction, gestione transazioni, Resource Manager e integrazione. Per altre informazioni, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model). Per le applicazioni che non riguardano la sicurezza, è possibile creare transazioni con elenchi di controllo di accesso (ACL) permissivi che consentono a qualsiasi gestore di risorse di integrarsi in una transazione.

## <a name="transactions"></a>Transazioni

Quando un client utilizza la funzione [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto transazione.

I diritti di accesso validi per gli oggetti transazione includono la possibilità di eseguire query e impostare informazioni, integrare e varie operazioni di transazione, oltre ai [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Maschere di accesso alle transazioni**](transaction-access-masks.md) elencano i diritti di accesso specifici per una transazione.

Poiché le transazioni hanno uno stato durevole, è fondamentale che RMs e TMs che interagiscono con il KTM soddisfino gli obblighi in relazione al ripristino. L'impossibilità di adempiere a questi obblighi può comportare perdite di risorse che non vengono rimosse, neanche dal riavvio del sistema. Si consideri l'effetto di una perdita persistente o di codice dannoso che ha causato l'utilizzo di risorse del kernel da parte di KTM finché non si è verificato un errore di sistema dopo il riavvio risultante, la KTM legge il log e ricrea tutti gli oggetti persistenti, causando potenzialmente lo stesso errore di sistema. La limitazione delle richieste basata sulla quota impedirà la persistenza di risorse persistenti da un RM non autorizzato o malintenzionato. Infine, è necessario creare meccanismi amministrativi che consentano il rilevamento e la correzione di tali perdite persistenti.

## <a name="transaction-managers"></a>Gestori transazioni

Quando un client usa la funzione [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto di Resource Manager.

I diritti di accesso validi per gli oggetti di gestione transazioni includono la possibilità di eseguire query e impostare informazioni, creare RMs, recuperare e rinominare operazioni, nonché [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Maschere di accesso di gestione transazioni**](transaction-manager-access-masks.md) elenca i diritti di accesso specifici per una gestione transazioni.

Un gestore di risorse può creare gli oggetti di gestione transazioni con ACL restrittivi per limitare i gestori di risorse che possono partecipare alle transazioni che utilizzano il log di tale gestore delle transazioni.

## <a name="resource-managers"></a>Gestione risorse

Quando un client usa la funzione [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto di Resource Manager.

I diritti di accesso validi per gli oggetti di Resource Manager includono la possibilità di eseguire query e impostare le informazioni, il ripristino, l'integrazione, le operazioni di registrazione e le operazioni di propagazione e ripristino, oltre ai [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Gestione risorse maschere di accesso**](resource-manager-access-masks.md) elenca i diritti di accesso specifici per un gestore di risorse.

Un gestore di risorse può creare propri oggetti Resource Manager con ACL restrittivi se desidera impedire a codice dannoso di intercettare le notifiche o forzare risultati transazionali specifici.

## <a name="enlistments"></a>Integrazioni

Quando un client utilizza la funzione [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto di integrazione.

I diritti di accesso validi per gli oggetti di integrazione includono la possibilità di eseguire query e impostare le informazioni, ripristinare le operazioni e [i diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Maschere di accesso all'elenco**](enlistment-access-masks.md) elenca i diritti di accesso specifici per un'integrazione.

 

 
