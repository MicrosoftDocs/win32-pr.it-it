---
title: Controllo dell'accesso agli oggetti e alle relative proprietà
description: Per controllare l'accesso agli oggetti applicazione, usare il descrittore di sicurezza dell'oggetto e, in particolare, con l'elenco di controllo di accesso discrezionale (DACL) e il relativo elenco di voci di controllo di accesso (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- oggetto AD, controllo dell'accesso a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220884"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>Controllo dell'accesso agli oggetti e alle relative proprietà

Per controllare l'accesso agli oggetti applicazione, usare il descrittore di sicurezza dell'oggetto e, in particolare, con l'elenco di controllo di accesso discrezionale (DACL) e il relativo elenco di voci di controllo di accesso (ACE).

Quando viene creato un oggetto, viene ricevuto un descrittore di sicurezza. Per ulteriori informazioni e per una descrizione delle regole utilizzate dal sistema per creare l'elenco DACL per un nuovo oggetto, vedere la pagina [relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](how-security-descriptors-are-set-on-new-directory-objects.md). Queste regole rivelano che è possibile:

-   Creare un nuovo descrittore di sicurezza e collegarlo all'oggetto al momento della creazione. Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto directory](creating-a-security-descriptor-for-a-new-directory-object.md).
-   Applicare una voce ACE ereditabile, in qualsiasi punto della gerarchia di directory, in modo che una voce ACE venga ereditata dagli oggetti nell'albero. Un oggetto può ereditare una voce ACE dal relativo contenitore padre. Per ulteriori informazioni, vedere [ereditarietà e delega dell'amministrazione](inheritance-and-delegation-of-administration.md).
-   Specificare una voce ACE nell'elenco DACL predefinito nello schema, se si dispone dei diritti di accesso necessari. Ogni definizione di classe di oggetto nello schema include un descrittore di sicurezza predefinito che può avere un DACL predefinito. Per ulteriori informazioni, vedere [descrittore di sicurezza predefinito](default-security-descriptor.md).

Inoltre, è possibile modificare l'elenco DACL di un oggetto esistente. È possibile:

-   Sostituire l'elenco DACL con uno nuovo.
-   Leggere l'elenco DACL esistente, modificarlo e applicare l'elenco DACL modificato. Per ulteriori informazioni, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Nell'elenco seguente viene descritta la funzione più importante di una voce ACE in Active Directory Domain Services. Con una voce ACE è possibile:

-   Controllare gli utenti che possono eseguire operazioni specifiche su un oggetto.
-   Controllo che ha accesso a una proprietà specifica o a un set di proprietà di un oggetto.
-   Controllare gli utenti che possono creare oggetti figlio in un contenitore, inclusi gli utenti che possono creare un tipo specifico di oggetto figlio.
-   Definire i diritti di accesso ai controlli privati per un tipo di oggetto e controllare chi può eseguire le operazioni protette da diritti privati.
-   Applicare una voce ACE a un oggetto contenitore alla radice di un sottoalbero di directory, in modo che le protezioni possano essere ereditate automaticamente da tutti gli oggetti figlio nella struttura ad albero.
-   Applicare una voce ACE ereditata automaticamente da un tipo specifico di oggetto figlio in un sottoalbero.
-   Creare una voce ACE che conceda diritti a un gruppo di sicurezza, anziché a un singolo utente.
-   Applicare una voce ACE a oggetti Criteri di gruppo per controllare gli account e i computer interessati dai criteri.

 

 




