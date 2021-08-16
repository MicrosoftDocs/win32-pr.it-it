---
description: Istruzioni per l'uso dell'API di Gestione autorizzazioni per definire le autorizzazioni in Script mediante la creazione di un archivio criteri di autorizzazione.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definizione delle autorizzazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 772c55f453a68e3bf1a4933abc4beb7cf3d65380b3bcf5d2e2c4af2832173b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782102"
---
# <a name="defining-permissions-in-script"></a>Definizione delle autorizzazioni nello script

In Gestione autorizzazioni è possibile definire gli utenti che hanno accesso alle risorse dell'applicazione creando un archivio criteri di autorizzazione.

**Per definire le autorizzazioni di accesso**

1.  Creare l'archivio in cui sono definiti i criteri di autorizzazione:<dl>

[Creazione di un archivio criteri di autorizzazione nello script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Creare una sezione nell'archivio dei criteri di autorizzazione per un'applicazione specifica:<dl>

[Creazione di un oggetto applicazione nello script](creating-an-application-object-in-script.md)  
    </dl>
3.  Definire le operazioni implementate dall'applicazione per accedere alle risorse e modificarle:<dl>

[Definizione di operazioni nello script](defining-operations-in-script.md)  
    </dl>
4.  Raggruppare le operazioni in attività di alto livello che gli utenti vogliono eseguire:<dl>

[Raggruppamento di operazioni in attività nello script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Definire i ruoli costituiti da gruppi di attività:<dl>

[Raggruppamento di attività in ruoli nello script](grouping-tasks-into-roles-in-script.md)  
    </dl>Un utente assegnato a un ruolo dispone dell'autorizzazione per eseguire qualsiasi attività assegnata a tale ruolo.
6.  Creare script per qualificare l'accesso alle attività in fase di esecuzione:<dl>

[Qualificazione dell'accesso con la logica di business nello script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Questo passaggio è facoltativo.
7.  Definire gruppi di utenti:<dl>

[Definizione di gruppi di utenti nello script](defining-groups-of-users-in-script.md)  
    </dl>Questi gruppi possono quindi essere assegnati ai ruoli per determinare quali attività possono eseguire.
8.  Aggiungere utenti ai gruppi di utenti:<dl>

[Aggiunta di utenti a un gruppo di applicazioni nello script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



