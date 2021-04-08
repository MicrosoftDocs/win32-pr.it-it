---
title: Controllo di accesso e operazioni di lettura
description: La sicurezza è un filtro implicito per la ricerca, l'enumerazione di contenitori o la lettura di proprietà.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Controllo di accesso e operazioni di lettura AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044017"
---
# <a name="access-control-and-read-operations"></a>Controllo di accesso e operazioni di lettura

La sicurezza è un filtro implicito per la ricerca, l'enumerazione di contenitori o la lettura di proprietà. Se non si dispone dei diritti di accesso necessari, i tentativi di elencare gli oggetti o le proprietà di lettura possono avere esito negativo con i codici di errore seguenti, anche se l'oggetto o la proprietà esiste:

-   **E \_ Ads \_ dominio non valido \_ \_**
-   **\_Proprietà Ads \_ E \_ non \_ supportata**
-   **\_Proprietà Ads \_ E \_ non \_ trovata**

Tenere presente che un chiamante con **Ads \_ Rights \_ ACTRL \_ DS \_ List** Access to a container può enumerare gli oggetti figlio nel contenitore. Tuttavia, un tentativo di accedere a un oggetto figlio può comunque avere esito negativo con un errore, ad esempio **E \_ Ads \_ Unknown \_ Object** se il chiamante non dispone di **Ads \_ right \_ ACTRL \_ \_ elenco DS \_** accesso all'oggetto figlio.

L'effetto della sicurezza sulle operazioni di lettura non è necessariamente manifesto come un errore. Ad esempio, un'operazione di ricerca può avere esito positivo, ma i risultati della ricerca non includono oggetti o proprietà a cui il chiamante non ha accesso.

 

 




