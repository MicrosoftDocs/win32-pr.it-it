---
description: Gestione risorse
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2ea9b1cd834daf3bfbca49bf37d3f2c0956344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311131"
---
# <a name="resource-managers"></a>Gestione risorse

Un gestore di risorse utilizza il log di gestione transazioni per tenere traccia dello stato della transazione. L'azione del gestore di risorse durante l'elaborazione di una transazione è la seguente:

-   Il client passa in modo esplicito una transazione a RM.
-   Il RM si integra nella transazione utilizzando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   L'utente può quindi continuare a eseguire qualsiasi operazione.
-   Quando l'utente chiama CommitTransaction, KTM invia una \_ notifica di preparazione transazione a RM. A questo punto, il RM Scarica su disco tutte le modifiche necessarie per eseguire il commit della transazione, ma potrebbe non riuscire. Se queste operazioni hanno esito positivo, il RM segnala che è terminato con l'operazione di preparazione chiamando [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete). Se queste operazioni hanno esito negativo, il RM risponde chiamando [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   Resource Manager riceve una notifica di preparazione.
-   Resource Manager Scarica tutti i dati associati alla transazione nel rispettivo file di log di log Services comune.
-   Resource Manager chiama la funzione [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) e attende di ricevere il risultato della transazione da KTM.
-   A seconda del risultato della transazione, gestione risorse riceve un evento di notifica di commit o di rollback. Se il gestore delle risorse riceve una notifica di commit, rende permanenti le modifiche e informa la KTM chiamando la funzione [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) . Se il gestore delle risorse riceve una notifica di rollback, rimuove tutte le modifiche e ripristina lo stato esistente prima di una delle modifiche transazionali e informa la KTM chiamando [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete).

## <a name="resource-manager-functions"></a>Funzioni Gestione risorse

Le funzioni seguenti vengono usate con i gestori di risorse.



| Funzione                                                                           | Descrizione                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Consente di creare un nuovo oggetto di Resource Manager (RM) e di associare RM a una gestione transazioni (TM).                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Richiede e riceve una notifica per Resource Manager (RM). Questa funzione viene utilizzata dal registro RM per ricevere notifiche quando lo stato di una transazione viene modificato.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Richiede e riceve una notifica asincrona per un gestore di risorse (RM). Questa funzione viene utilizzata dal registro RM per ricevere notifiche quando lo stato di una transazione viene modificato. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Apre un gestore di risorse esistente (RM).                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica che Gestione risorse ha completato tutte le operazioni di elaborazione necessarie per garantire l'esito positivo di un'operazione di commit o di interruzione per la transazione specificata.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Segnala che questo gestore di risorse ha completato il lavoro di prepreparazione, in modo che gli altri gestori di risorse possano ora iniziare le operazioni di preparazione.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa la porta di completamento di I/O specificata al gestore di risorse specificato (RM). Questa porta riceve tutte le notifiche per RM.                                          |



 

 

 



