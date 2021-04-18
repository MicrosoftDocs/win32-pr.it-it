---
description: Usare l'API di gestione autorizzazioni per controllare l'accesso alle risorse dell'applicazione.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Utilizzo dell'autorizzazione in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315424"
---
# <a name="using-authorization-in-c"></a>Utilizzo dell'autorizzazione in C++

È possibile utilizzare l'API di gestione autorizzazioni per controllare l'accesso alle risorse dell'applicazione.

Se si dispone di una soluzione di controllo degli accessi esistente basata sugli [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) e si vuole evitare di convertire questa soluzione per l'uso di gestione autorizzazioni, è possibile continuare a usare gli ACL per controllare l'accesso alle risorse. Per informazioni sul controllo dell'accesso alle risorse tramite gli ACL, vedere [definizione delle autorizzazioni con ACL in c++](defining-permissions-with-acls-in-c--.md), [creazione di un contesto client da un SID in c++](establishing-a-client-context-from-a-sid-in-c--.md)e [Verifica dell'accesso client con ACL in c++](verifying-client-access-with-acls-in-c--.md).

> [!Note]  
> Per le aziende di grandi dimensioni, esiste un compromesso tra il sovraccarico amministrativo e le prestazioni. Con l'aumentare del numero di risorse e utenti protetti, l'amministrazione degli ACL diventa più complessa. Le prestazioni non vengono compromesse perché tutte le informazioni necessarie sui diritti di accesso vengono distribuite alle risorse protette. Le prestazioni di gestione autorizzazioni sono influenzate dalla scalabilità.

 

Per informazioni sulle altre attività di autorizzazione, vedere [supporto di attività per l'autorizzazione in C++](supporting-tasks-for-authorization-in-c--.md).



| Argomento                                                                                                                | Descrizione                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definizione delle autorizzazioni in C++](defining-permissions-in-c--.md)                                                       | Definire gli utenti che possono accedere alle risorse dell'applicazione creando un archivio dei criteri di autorizzazione. |
| [Verifica dell'accesso client a una risorsa richiesta in C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Controllare se il client ha accesso a una o più operazioni.                                           |
| [Delega della definizione di autorizzazioni in C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory.          |



 

 

 
