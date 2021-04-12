---
title: Come vengono impostati i descrittori di sicurezza per i nuovi oggetti directory
description: Quando si crea un nuovo oggetto in Active Directory Domain Services, è possibile creare in modo esplicito un descrittore di sicurezza e quindi impostare il descrittore di sicurezza come proprietà nTSecurityDescriptor dell'oggetto.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- oggetti AD, come vengono impostati i descrittori di sicurezza per i nuovi oggetti directory
- descrittori di sicurezza AD, come impostare per i nuovi oggetti directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472539"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Come vengono impostati i descrittori di sicurezza per i nuovi oggetti directory

Quando si crea un nuovo oggetto in Active Directory Domain Services, è possibile creare in modo esplicito un descrittore di sicurezza e quindi impostare il descrittore di sicurezza come proprietà **ntSecurityDescriptor** dell'oggetto. Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto directory](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services utilizzare le seguenti regole per impostare l'elenco DACL nel descrittore di sicurezza del nuovo oggetto:

-   Se si specifica in modo esplicito un descrittore di sicurezza quando si crea l'oggetto, il sistema unisce eventuali ACE ereditabili dall'oggetto padre nell'elenco DACL specificato, a meno che il bit non **\_ \_ protetto DACL** non sia impostato nei bit di controllo del descrittore di sicurezza.
-   Se non si specifica un descrittore di sicurezza, il sistema compila l'elenco DACL dell'oggetto unendo eventuali ACE ereditabili dall'oggetto padre nell'elenco DACL predefinito dall'oggetto **classSchema** per la classe dell'oggetto.
-   Se lo schema non dispone di un DACL predefinito, il DACL dell'oggetto è l'elenco DACL predefinito del token primario o di rappresentazione del creatore.
-   Se non è presente alcun DACL specificato, ereditato o predefinito, il sistema crea l'oggetto senza DACL, che consente a tutti gli utenti di accedere completamente all'oggetto.

Il sistema usa un algoritmo simile per creare un SACL per un oggetto servizio directory.

Il proprietario e il gruppo primario nel descrittore di sicurezza del nuovo oggetto sono impostati sui valori specificati nella proprietà **ntSecurityDescriptor** quando si crea l'oggetto. Se non si impostano questi valori, Active Directory Domain Services utilizzare le regole elencate nella tabella seguente per impostarle.



| Regola          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proprietario         | Il proprietario in un descrittore di sicurezza predefinito è impostato sul SID del proprietario predefinito dal token primario o di rappresentazione del processo di creazione. Per la maggior parte degli utenti, il SID del proprietario predefinito corrisponde al SID che identifica l'account dell'utente. Tenere presente che per gli utenti che sono membri del gruppo Administrators predefinito, il sistema imposta automaticamente il SID predefinito del proprietario nel token di accesso per il gruppo Administrators. di conseguenza, gli oggetti creati da un membro del gruppo Administrators sono in genere di proprietà del gruppo Administrators. Per ottenere o impostare il proprietario predefinito in un token di accesso, chiamare la funzione [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la struttura del [**\_ proprietario del token**](/windows/desktop/api/winnt/ns-winnt-token_owner) . |
| Gruppo primario | Il gruppo primario in un descrittore di sicurezza predefinito è impostato sul gruppo primario predefinito dal token primario o di rappresentazione del creatore. Tenere presente che il gruppo primario non viene utilizzato nel contesto di Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Per ulteriori informazioni sull'ereditarietà ACE, vedere [ereditarietà e delega dell'amministrazione](inheritance-and-delegation-of-administration.md).

Per ulteriori informazioni sui descrittori di sicurezza predefiniti nello schema, vedere [descrittore di sicurezza predefinito](default-security-descriptor.md).

Per ulteriori informazioni sugli oggetti **classSchema** , vedere [Active Directory schema](active-directory-schema.md).

 

 