---
title: Che cos'è un utente
description: Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- Che cos'è un utente Active Directory
- utenti Active Directory, che cos'è un utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c59b2ea46474860268f327bcd03d2ba67ecea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707504"
---
# <a name="what-is-a-user"></a>Che cos'è un utente?

Gli account utente vengono creati e archiviati come oggetti in Active Directory Domain Services. Gli account utente possono essere utilizzati da utenti o programmi umani, ad esempio i servizi di sistema, per accedere a un computer. Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con i dati archiviati nell'oggetto utente dell'utente nel server Active Directory. Se la password viene autenticata, ovvero la password visualizzata corrisponde alla password archiviata nell'oggetto utente, il sistema genera un token di accesso. Un token di accesso è un oggetto che descrive il contesto di sicurezza di un processo o di un thread. I dati in un token includono l'identità di sicurezza e l'appartenenza a gruppi dell'account utente associato al processo o al thread. Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.

Ogni utente o applicazione che accede alle risorse in un dominio Windows deve disporre di un account nel server Active Directory. Windows utilizza questo account utente per verificare che l'utente o l'applicazione disponga delle autorizzazioni per l'utilizzo di una risorsa.

Un account utente può essere usato per:

-   Consentire agli utenti umani di accedere a un computer e accedere alle risorse in base all'identità dell'account utente.
-   Consentire l'esecuzione di programmi e servizi in un contesto di sicurezza specifico.
-   Consente di gestire l'accesso degli utenti alle risorse condivise, ad esempio gli oggetti e le relative proprietà, condivisioni di rete, file, directory, code di stampanti e così via.

I gruppi possono contenere membri, che fanno riferimento a utenti e altri gruppi. I gruppi possono essere usati anche per controllare l'accesso alle risorse condivise. Quando si assegnano le autorizzazioni per le risorse, ad esempio condivisioni file, stampanti e così via, gli amministratori devono assegnare tali autorizzazioni a un gruppo anziché ai singoli utenti. Le autorizzazioni vengono assegnate una volta al gruppo, anziché più volte a ogni singolo utente. Ciò consente di semplificare la manutenzione e l'amministrazione di una rete.

## <a name="users-compared-to-contacts"></a>Utenti confrontati con contatti

Sia gli utenti che i contatti possono essere usati per rappresentare gli utenti umani. Tuttavia, un utente è un'entità di sicurezza. non è presente alcun contatto.

Un utente può essere usato per consentire a un utente umano di accedere e accedere alle risorse condivise.

Un contatto viene usato solo per la lista di distribuzione e per gli scopi di posta elettronica. Un contatto, tuttavia, può contenere la maggior parte dei dati archiviati in un oggetto utente, ad esempio indirizzo, numeri di telefono e così via, perché sia utente che contatto derivano dall'oggetto Person **classSchema** . Un contatto non dispone di un contesto di sicurezza. Pertanto, non è possibile utilizzare un contatto per controllare l'accesso alle risorse condivise e non può essere utilizzato per accedere a un computer.

## <a name="users-compared-to-computers"></a>Utenti confrontati con computer

La classe dell'oggetto computer eredita dalla classe dell'oggetto utente. Un oggetto computer rappresenta un computer; Tuttavia, il computer e i servizi locali del computer richiedono spesso l'accesso alla rete e alle risorse condivise. Quando il computer accede a risorse condivise, non all'utente connesso al computer, è necessario un token di accesso, proprio come un utente umano che ha eseguito l'accesso come utente. Quando un computer accede alla rete, utilizza un token di accesso che contiene l'ID di sicurezza per l'account computer del computer e i gruppi di cui l'account è membro.

Un servizio può essere eseguito nel contesto di LocalSystem o di un account del servizio specifico. Nei computer che eseguono Windows 2000, un servizio che viene eseguito nel contesto dell'account LocalSystem usa le credenziali del computer.

 

 




