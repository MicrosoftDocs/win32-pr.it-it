---
description: Istruzioni per l'uso dell'API di gestione autorizzazioni per definire le autorizzazioni in C++ creando un archivio dei criteri di autorizzazione.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definizione delle autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319918"
---
# <a name="defining-permissions-in-c"></a>Definizione delle autorizzazioni in C++

In Gestione autorizzazioni è possibile definire quali utenti hanno accesso alle risorse dell'applicazione creando un archivio criteri di autorizzazione.

Per informazioni sulla definizione delle autorizzazioni con ACL, vedere [definizione delle autorizzazioni con ACL in C++](defining-permissions-with-acls-in-c--.md).

**Per definire le autorizzazioni di accesso**

1.  Creare l'archivio in cui sono definiti i criteri di autorizzazione:<dl>

[Creazione di un oggetto archivio criteri di autorizzazione in C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Creare una sezione nell'archivio dei criteri di autorizzazione per un'applicazione specifica:<dl>

[Creazione di un oggetto applicazione in C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Definire le operazioni implementate dall'applicazione per accedere alle risorse e modificarle:<dl>

[Definizione di operazioni in C++](defining-operations-in-c--.md)  
    </dl>
4.  Raggruppare le operazioni in attività di alto livello che gli utenti desiderano eseguire:<dl>

[Raggruppamento di operazioni in attività in C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definire i ruoli che sono costituiti da gruppi di attività:<dl>

[Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Un utente assegnato a un ruolo dispone dell'autorizzazione per eseguire tutte le attività assegnate a tale ruolo.
6.  Creare script per qualificare l'accesso alle attività in fase di esecuzione:<dl>

[Qualificazione dell'accesso con la logica di business in C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Questo passaggio è facoltativo.
7.  Definire gruppi di utenti:<dl>

[Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)  
    </dl>Questi gruppi possono quindi essere assegnati ai ruoli per determinare quali attività possono essere eseguite.
8.  Aggiungere utenti ai gruppi di utenti:<dl>

[Aggiunta di utenti a un gruppo di applicazioni in C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



