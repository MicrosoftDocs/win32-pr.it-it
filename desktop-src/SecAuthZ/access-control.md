---
description: Il controllo di accesso si riferisce alle funzionalità di sicurezza che controllano gli utenti che possono accedere alle risorse nel sistema operativo. Le applicazioni chiamano funzioni di controllo di accesso per impostare gli utenti che possono accedere a risorse specifiche o controllare l'accesso alle risorse fornite dall'applicazione.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Controllo di accesso (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049894"
---
# <a name="access-control-authorization"></a>Controllo di accesso (autorizzazione)

Il controllo di accesso si riferisce alle funzionalità di sicurezza che controllano gli utenti che possono accedere alle risorse nel sistema operativo. Le applicazioni chiamano funzioni di controllo di accesso per impostare gli utenti che possono accedere a risorse specifiche o controllare l'accesso alle risorse fornite dall'applicazione.

In questa panoramica viene descritto il modello di sicurezza per controllare l'accesso agli oggetti di Windows, ad esempio i file, e per controllare l'accesso alle funzioni amministrative, ad esempio l'impostazione dell'ora di sistema o il controllo delle azioni dell'utente. Nell'argomento [modello di controllo di accesso](access-control-model.md) viene fornita una descrizione di alto livello delle parti del controllo di accesso e del modo in cui interagiscono tra loro.

Negli argomenti seguenti viene descritto il controllo degli accessi:

-   [Sicurezza a livello C2](c2-level-security.md)
-   [Modello di controllo di accesso](access-control-model.md)
-   [Linguaggio di definizione del descrittore di sicurezza](security-descriptor-definition-language.md)
-   [Privilegi](privileges.md)
-   [Generazione di controllo](audit-generation.md)
-   [Oggetti a protezione diretta](securable-objects.md)
-   [Controllo di accesso di basso livello](low-level-access-control.md)

Di seguito sono riportate le attività comuni di controllo di accesso:

-   [Come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md)
-   [Controllo della creazione di oggetti figlio in C++](controlling-child-object-creation-in-c--.md)
-   [ACE per controllare l'accesso alle proprietà di un oggetto](aces-to-control-access-to-an-object-s-properties.md)
-   [Richiesta di diritti di accesso a un oggetto](requesting-access-rights-to-an-object.md)

Negli argomenti seguenti viene fornito il codice di esempio per le attività di controllo di accesso:

-   [Modifica degli ACL di un oggetto in C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Creazione di un descrittore di sicurezza per un nuovo oggetto in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Controllo della creazione di oggetti figlio in C++](controlling-child-object-creation-in-c--.md)
-   [Abilitazione e disabilitazione dei privilegi in C++](enabling-and-disabling-privileges-in-c--.md)
-   [Ricerca di un SID in un token di accesso in C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Ricerca del proprietario di un oggetto file in C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Assunzione della proprietà di un oggetto in C++](taking-object-ownership-in-c--.md)
-   [Creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
