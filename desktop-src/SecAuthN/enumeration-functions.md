---
description: Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti. MPR chiama queste funzioni per enumerare le risorse.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funzioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049426"
---
# <a name="enumeration-functions"></a>Funzioni di enumerazione

Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti. MPR chiama queste funzioni per enumerare le risorse.

Non è necessario un provider di rete per implementare alcuna delle funzioni di enumerazione. Se, tuttavia, un provider di rete implementa [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)o [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), deve implementare anche le altre due funzioni di enumerazione.



| Funzione                                                     | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Apre un'enumerazione delle risorse di rete o delle connessioni esistenti.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Esegue un'enumerazione su un handle restituito da [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Chiude un'enumerazione.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Determina se il provider è il provider corretto per rispondere a una richiesta per una risorsa di rete specificata e restituisce informazioni sul tipo di risorsa. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Restituisce l'elemento padre di una risorsa di rete specificata nella gerarchia browse.                                                                                         |



 

 

 



