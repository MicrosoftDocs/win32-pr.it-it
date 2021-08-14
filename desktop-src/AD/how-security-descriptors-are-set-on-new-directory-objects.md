---
title: Impostazione dei descrittori di sicurezza per i nuovi oggetti directory
description: Quando si crea un nuovo oggetto in Active Directory Domain Services, è possibile creare in modo esplicito un descrittore di sicurezza e quindi impostare tale descrittore di sicurezza come proprietà nTSecurityDescriptor dell'oggetto.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- oggetti AD, modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory
- descrittori di sicurezza AD, come impostare su nuovi oggetti directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d2009367c4d5604d359913b0154320332cd4be58e50dc5f065c574f8ea5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188112"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Impostazione dei descrittori di sicurezza per i nuovi oggetti directory

Quando si crea un nuovo oggetto in Active Directory Domain Services, è possibile creare in modo esplicito un descrittore di sicurezza e quindi impostare tale descrittore di sicurezza come proprietà **nTSecurityDescriptor** dell'oggetto. Per altre informazioni, vedere [Creazione di un descrittore di sicurezza per un nuovo oggetto directory.](creating-a-security-descriptor-for-a-new-directory-object.md)

Active Directory Domain Services usare le regole seguenti per impostare l'elenco DACL nel descrittore di sicurezza del nuovo oggetto:

-   Se si specifica in modo esplicito un descrittore di sicurezza quando si crea l'oggetto, il sistema unisce tutte le ACE ereditabili dall'oggetto padre nell'elenco DACL specificato, a meno che il bit **\_ edizione Standard DACL \_ PROTECTED** non sia impostato nei bit di controllo del descrittore di sicurezza.
-   Se non si specifica un descrittore di sicurezza, il sistema compila l'elenco DACL dell'oggetto unendo tutte le voci ACE ereditabili dall'oggetto padre nell'elenco DACL predefinito dall'oggetto **classSchema** per la classe dell'oggetto.
-   Se lo schema non dispone di un DACL predefinito, l'elenco DACL dell'oggetto è l'elenco DACL predefinito del token primario o di rappresentazione dell'autore.
-   Se non è presente alcun DACL specificato, ereditato o predefinito, il sistema crea l'oggetto senza DACL, che consente a tutti l'accesso completo all'oggetto.

Il sistema usa un algoritmo simile per compilare un SACL per un oggetto servizio directory.

Il proprietario e il gruppo primario nel descrittore di sicurezza del nuovo oggetto vengono impostati su valori specificati nella proprietà **nTSecurityDescriptor** quando si crea l'oggetto. Se non si impostano questi valori, Active Directory Domain Services usare le regole elencate nella tabella seguente per impostarli.



| Regola          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proprietario         | Il proprietario in un descrittore di sicurezza predefinito è impostato sul SID del proprietario predefinito dal token primario o di rappresentazione del processo di creazione. Per la maggior parte degli utenti, il SID proprietario predefinito corrisponde al SID che identifica l'account dell'utente. Tenere presente che per gli utenti membri del gruppo administrators predefinito, il sistema imposta automaticamente il SID del proprietario predefinito nel token di accesso sul gruppo administrators. Pertanto, gli oggetti creati da un membro del gruppo Administrators sono in genere di proprietà del gruppo Administrators. Per ottenere o impostare il proprietario predefinito in un token di accesso, chiamare la [**funzione GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la [**struttura TOKEN \_ OWNER.**](/windows/desktop/api/winnt/ns-winnt-token_owner) |
| Gruppo primario | Il gruppo primario in un descrittore di sicurezza predefinito è impostato sul gruppo primario predefinito dal token di rappresentazione o primario dell'autore. Tenere presente che il gruppo primario non viene usato nel contesto di Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Per altre informazioni sull'ereditarietà ACE, vedere [Ereditarietà e delega dell'amministrazione.](inheritance-and-delegation-of-administration.md)

Per altre informazioni sui descrittori di sicurezza predefiniti nello schema, vedere [Descrittore di sicurezza predefinito.](default-security-descriptor.md)

Per altre informazioni sugli **oggetti classSchema,** vedere [Schema di Active Directory.](active-directory-schema.md)

 

 