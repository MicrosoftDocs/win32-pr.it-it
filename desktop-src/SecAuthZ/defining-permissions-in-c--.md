---
description: Istruzioni per l'uso dell'API di Gestione autorizzazioni per definire le autorizzazioni in C++ creando un archivio criteri di autorizzazione.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definizione delle autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008c82e74bcd4b4fec714e43c8beb7d8c7e908baaf569ee260559f64ba5bbc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913774"
---
# <a name="defining-permissions-in-c"></a>Definizione delle autorizzazioni in C++

In Gestione autorizzazioni è possibile definire gli utenti che hanno accesso alle risorse dell'applicazione creando un archivio criteri di autorizzazione.

Per informazioni sulla definizione delle autorizzazioni con gli ACL, vedere Definizione delle autorizzazioni con gli [ACL in C++.](defining-permissions-with-acls-in-c--.md)

**Per definire le autorizzazioni di accesso**

1.  Creare l'archivio in cui sono definiti i criteri di autorizzazione:<dl>

[Creazione di un oggetto archivio criteri di autorizzazione in C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Creare una sezione nell'archivio criteri di autorizzazione per un'applicazione specifica:<dl>

[Creazione di un oggetto applicazione in C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Definire le operazioni implementate dall'applicazione per accedere alle risorse e modificarle:<dl>

[Definizione di operazioni in C++](defining-operations-in-c--.md)  
    </dl>
4.  Raggruppare le operazioni in attività di alto livello che gli utenti vogliono eseguire:<dl>

[Raggruppamento di operazioni in attività in C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definire ruoli costituiti da gruppi di attività:<dl>

[Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Un utente assegnato a un ruolo dispone dell'autorizzazione per eseguire qualsiasi attività assegnata a tale ruolo.
6.  Creare script per qualificare l'accesso alle attività in fase di esecuzione:<dl>

[Qualifica dell'accesso con la logica di business in C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Questo passaggio è facoltativo.
7.  Definire gruppi di utenti:<dl>

[Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)  
    </dl>Questi gruppi possono quindi essere assegnati ai ruoli per determinare le attività che possono eseguire.
8.  Aggiungere utenti ai gruppi di utenti:<dl>

[Aggiunta di utenti a un gruppo di applicazioni in C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



