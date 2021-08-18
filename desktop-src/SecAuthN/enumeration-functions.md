---
description: Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti. La funzione MPR chiama queste funzioni per enumerare le risorse.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funzioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f119256c4976e393795b45caf2fab9e7cec5353fed54718ef0be8db994ef2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008239"
---
# <a name="enumeration-functions"></a>Funzioni di enumerazione

Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti. La funzione MPR chiama queste funzioni per enumerare le risorse.

Non è necessario un provider di rete per implementare alcuna funzione di enumerazione. Se, tuttavia, un provider di rete implementa [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)o [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), deve implementare anche le altre due funzioni di enumerazione.



| Funzione                                                     | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Apre un'enumerazione di risorse di rete o connessioni esistenti.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Esegue un'enumerazione su un handle restituito da [**NPOpenEnum.**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Chiude un'enumerazione.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Determina se il provider è il provider corretto per rispondere a una richiesta per una risorsa di rete specificata e restituisce informazioni sul tipo della risorsa. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Restituisce l'elemento padre di una risorsa di rete specificata nella gerarchia di esplorazione.                                                                                         |



 

 

 



