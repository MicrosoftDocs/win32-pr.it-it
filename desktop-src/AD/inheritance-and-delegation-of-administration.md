---
title: Ereditarietà e delega dell'amministrazione
description: Viene descritto il supporto di servizi di dominio Active Directory per l'ereditarietà delle autorizzazioni nell'albero degli oggetti e anche l'ereditarietà specifica dell'oggetto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- ereditarietà dell'amministrazione e delega Active Directory
- Active Directory Active Directory, ereditarietà delle autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220933"
---
# <a name="inheritance-and-delegation-of-administration"></a>Ereditarietà e delega dell'amministrazione

Active Directory Domain Services supporta l'ereditarietà delle autorizzazioni nell'albero degli oggetti per consentire l'esecuzione delle attività di amministrazione a livelli più elevati nell'albero. Ciò consente agli amministratori di configurare le autorizzazioni ereditabili sugli oggetti vicini alla radice, ad esempio le unità di dominio e organizzative, e di distribuire tali autorizzazioni a vari oggetti dell'albero.

L'ereditarietà può essere impostata in base a ACE. Nella tabella seguente sono elencati i flag che è possibile specificare in **AceFlags** per controllare l'ereditarietà della voce ACE.



| Flag                                                     | Descrizione                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ eredita \_ ACE**<br/>                | Determina l'ereditarietà della voce ACE nell'albero.<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ No \_ propagate \_ eredita \_ ACE**<br/> | Determina l'ereditarietà della voce ACE su un solo livello nell'albero.<br/>                                                                      |
| **ADS \_ ACEFLAG \_ ereditano \_ solo \_ ACE**<br/>          | Fa in modo che la voce ACE venga ignorata sull'oggetto su cui è specificato, che venga ereditata solo in basso ed è valida in cui è stata ereditata.<br/> |



 

Oltre a impostare l'ereditarietà, Active Directory Domain Services supporta l'ereditarietà specifica dell'oggetto. In questo modo, le voci ACE ereditabili possono essere ereditate dall'albero, ma sono valide solo per un tipo specifico di oggetto. Questa operazione è estremamente utile per delegare l'amministrazione. Ad esempio, può essere usato per impostare una voce ACE ereditabile specifica dell'oggetto in un'unità organizzativa che consente a un gruppo di avere il controllo completo su tutti gli oggetti utente nell'unità organizzativa, ma nient'altro. In questo modo, la gestione degli utenti in tale unità organizzativa viene delegata agli utenti di tale gruppo.

### <a name="delegating-service-administration-with-security-groups"></a>Delega dell'amministrazione del servizio con gruppi di sicurezza

Usare i gruppi di sicurezza per definire e delegare i ruoli amministrativi associati al server applicazioni. Ad esempio, il servizio può essere associato a un gruppo amministratori di servizi. Gli utenti che sono identificati come amministratori del servizio verranno aggiunti al gruppo di amministratori del servizio. Il programma di installazione per il servizio può impostare gli ACL nella directory per consentire agli amministratori del servizio di disporre di autorizzazioni sufficienti per la lettura/scrittura degli attributi correlati al servizio o per la creazione di oggetti specifici del servizio, ad esempio.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Ruoli nei gruppi di sicurezza per i computer che eseguono il servizio

Usare i gruppi di sicurezza per definire il set di computer a cui viene concesso l'accesso agli oggetti del servizio nella directory. Ad esempio, il servizio può essere associato a un server Servizi di gruppo. Tutti i computer in cui è in esecuzione il server di servizio vengono aggiunti al gruppo di server di servizio e a questo gruppo può essere concesso l'accesso alle parti della directory in cui i server dei servizi devono leggere/scrivere i dati. Il programma di installazione per il servizio può impostare gli ACL nella directory per consentire ai server di servizi di disporre di autorizzazioni sufficienti per la lettura/scrittura degli attributi correlati al servizio o per la creazione di oggetti specifici del servizio, ad esempio.

 

 





