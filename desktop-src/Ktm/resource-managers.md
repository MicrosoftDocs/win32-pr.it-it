---
description: Resource Manager
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d32d697d58705760002065d005f5927717055f235358c12fd0629de86e14b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870021"
---
# <a name="resource-managers"></a>Resource Manager

Un gestore di risorse utilizza il log di gestione transazioni per tenere traccia dello stato della transazione. L'azione del gestore di risorse durante l'elaborazione di una transazione è la seguente:

-   Il client passa una transazione all'RM in modo esplicito.
-   L'RM si integra nella transazione usando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   L'utente può quindi procedere con qualsiasi operazione.
-   Quando l'utente chiama CommitTransaction, KTM invia una notifica PREPARE \_ TRANSACTION all'RM. A questo punto, l'RM scarica su disco tutte le modifiche necessarie per eseguire il commit della transazione, ma potrebbe non riuscire. Se queste operazioni hanno esito positivo, l'RM segnala che è stata completata con l'operazione di preparazione chiamando [**PrepareComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) Se queste operazioni hanno esito negativo, l'RM risponde chiamando [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   Il gestore di risorse riceve una notifica di preparazione.
-   Il gestore di risorse scarica tutti i dati associati alla transazione nel relativo file di log di Common Log Services.
-   Il gestore di risorse chiama [**la funzione PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) e attende di ricevere il risultato della transazione dal KTM.
-   A seconda del risultato della transazione, il gestore delle risorse riceve un evento di notifica di commit o rollback. Se il gestore di risorse riceve una notifica di commit, rende permanenti le modifiche e informa KTM chiamando la [**funzione CommitComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) Se il gestore delle risorse riceve una notifica di rollback, rimuove tutte le modifiche e ripristina lo stato esistente prima di una delle modifiche transazionate e informa KTM chiamando [**RollbackComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)

## <a name="resource-manager-functions"></a>Resource Manager funzioni

Le funzioni seguenti vengono usate con i gestori di risorse.



| Funzione                                                                           | Descrizione                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuovo oggetto gestione risorse (RM) e associa l'RM a una gestione transazioni.                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Richiede e riceve una notifica per un gestore di risorse (RM). Questa funzione viene usata dal registro RM per ricevere notifiche quando lo stato di una transazione cambia.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Richiede e riceve una notifica asincrona per un gestore di risorse (RM). Questa funzione viene usata dal registro RM per ricevere notifiche quando lo stato di una transazione cambia. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Apre un gestore di risorse (RM) esistente.                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica che il gestore di risorse (RM) ha completato tutte le elaborazioni necessarie per garantire che un'operazione di commit o interruzione abbia esito positivo per la transazione specificata.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Segnala che questo gestore di risorse ha completato il lavoro di preprepare, in modo che gli altri gestori di risorse possano ora iniziare le operazioni di preparazione.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa la porta di completamento I/O specificata al gestore delle risorse (RM) specificato. Questa porta riceve tutte le notifiche per l'RM.                                          |



 

 

 



