---
description: Il sistema utilizza oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informazioni sugli handle e sugli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967605"
---
# <a name="about-handles-and-objects"></a>Informazioni sugli handle e sugli oggetti

Il sistema utilizza oggetti e handle per regolare l'accesso alle risorse di sistema per due motivi principali. In primo luogo, l'utilizzo di oggetti garantisce che Microsoft possa aggiornare la funzionalità di sistema, purché venga mantenuta l'interfaccia dell'oggetto originale. Quando vengono rilasciate le versioni successive del sistema, è possibile utilizzare l'oggetto aggiornato con un numero di lavoro aggiuntivo o minimo.

In secondo luogo, l'utilizzo di oggetti consente di sfruttare la sicurezza di Windows. Ogni oggetto dispone di un proprio elenco di controllo di accesso (ACL) che specifica le azioni che possono essere eseguite da un processo sull'oggetto. Il sistema esamina l'elenco di controllo di accesso di un oggetto ogni volta che un'applicazione crea un handle per l'oggetto. Per altre informazioni, vedere [Controllo di accesso](/windows/desktop/SecAuthZ/access-control).

-   [Gestore oggetti](object-manager.md)
-   [Interfaccia oggetto](object-interface.md)
-   [Spazi dei nomi degli oggetti](/windows/desktop/Sync/object-namespaces)
-   [Limitazioni della gestione](handle-limitations.md)
-   [Gestisci ereditarietà](handle-inheritance.md)

 

 
