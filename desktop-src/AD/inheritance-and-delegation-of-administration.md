---
title: Ereditarietà e delega dell'amministrazione
description: Viene descritto il supporto di Servizi di dominio Active Directory per l'ereditarietà delle autorizzazioni nella struttura ad albero di oggetti e anche per l'ereditarietà specifica dell'oggetto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- amministrazione ereditarietà e delega di Active Directory
- Active Directory Active Directory , ereditarietà delle autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b48ff4d913cbd8bf16f7b2c67adf86d61515298dcac267291641d30504e1e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187524"
---
# <a name="inheritance-and-delegation-of-administration"></a>Ereditarietà e delega dell'amministrazione

Active Directory Domain Services supporta l'ereditarietà delle autorizzazioni nella struttura ad albero di oggetti per consentire l'esecuzione delle attività di amministrazione a livelli superiori nell'albero. In questo modo gli amministratori possono configurare autorizzazioni ereditabili per gli oggetti vicini alla radice, ad esempio unità organizzative e dominio, e avere tali autorizzazioni distribuite a vari oggetti nell'albero.

L'ereditarietà può essere impostata per ogni ACE. Nella tabella seguente sono elencati i flag che è possibile specificare in **AceFlags per** controllare l'ereditarietà della ACE.



| Flag                                                     | Descrizione                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ INHERIT \_ ACE**<br/>                | Fa sì che la ACE sia ereditata nell'albero.<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ NO \_ PROPAGATE \_ INHERIT \_ ACE**<br/> | Fa sì che la ACE sia ereditata di un solo livello nell'albero.<br/>                                                                      |
| **ADS \_ ACEFLAG \_ INHERIT \_ ONLY \_ ACE**<br/>          | Fa in modo che la ACE sia ignorata nell'oggetto in cui è specificata, che sia ereditata solo e sia efficace nel punto in cui è stata ereditata.<br/> |



 

Oltre a impostare l'ereditarietà, Active Directory Domain Services supporta l'ereditarietà specifica dell'oggetto. In questo modo le voci ACE ereditabili possono essere ereditate lungo l'albero, ma essere efficaci solo su un tipo specifico di oggetto. Ciò è estremamente utile per delegare l'amministrazione. Ad esempio, può essere usato per impostare una ACE ereditabile specifica dell'oggetto in un'unità organizzativa che consente a un gruppo di avere il controllo completo su tutti gli oggetti utente nell'unità organizzativa, ma non altro. Di conseguenza, la gestione degli utenti in tale unità organizzativa viene delegata agli utenti in tale gruppo.

### <a name="delegating-service-administration-with-security-groups"></a>Delega dell'amministrazione del servizio con i gruppi di sicurezza

Usare i gruppi di sicurezza per definire e delegare i ruoli amministrativi associati al server applicazioni. Ad esempio, il servizio può essere associato a un gruppo MyService Administrators. Gli utenti identificati come amministratori di MyService verranno aggiunti al gruppo MyService Administrators. Il programma di installazione per MyService può impostare elenchi di controllo di accesso nella directory per consentire agli amministratori di MyService autorizzazioni sufficienti per leggere/scrivere attributi correlati a MyService o creare oggetti specifici di MyService, ad esempio.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Ruoli nei gruppi di sicurezza per i computer che eseguono il servizio

Usare i gruppi di sicurezza per definire il set di computer a cui viene concesso l'accesso agli oggetti del servizio nella directory. Ad esempio, il servizio può essere associato a un gruppo MyService Servers. Tutti i computer che eseguono il server MyService vengono aggiunti al gruppo MyService Servers e a questo gruppo può quindi essere assegnato l'accesso alle parti della directory in cui i server MyService devono leggere/scrivere dati. Il programma di installazione per MyService può impostare elenchi di controllo di accesso nella directory per abilitare i server MyService autorizzazioni sufficienti per leggere/scrivere attributi correlati a MyService o creare oggetti specifici di MyService, ad esempio.

 

 





