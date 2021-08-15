---
description: Il sistema usa oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informazioni su handle e oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eee99e0568a0535462e89bfd5de71e12cfaf4a588a605f190dba41ce0ef2535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959049"
---
# <a name="about-handles-and-objects"></a>Informazioni su handle e oggetti

Il sistema usa oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali. In primo luogo, l'uso di oggetti garantisce che Microsoft possa aggiornare le funzionalità di sistema, purché l'interfaccia degli oggetti originale sia mantenuta. Quando vengono rilasciate versioni successive del sistema, è possibile usare l'oggetto aggiornato con poco o nessun lavoro aggiuntivo.

In secondo luogo, l'uso di oggetti consente di sfruttare Windows sicurezza. Ogni oggetto ha un proprio elenco di controllo di accesso (ACL) che specifica le azioni che un processo può eseguire sull'oggetto. Il sistema esamina l'ACL di un oggetto ogni volta che un'applicazione crea un handle per l'oggetto. Per altre informazioni, vedere [Controllo di accesso](/windows/desktop/SecAuthZ/access-control).

-   [Gestione oggetti](object-manager.md)
-   [Interfaccia dell'oggetto](object-interface.md)
-   [Spazi dei nomi degli oggetti](/windows/desktop/Sync/object-namespaces)
-   [Gestire le limitazioni](handle-limitations.md)
-   [Gestire l'ereditarietà](handle-inheritance.md)

 

 
