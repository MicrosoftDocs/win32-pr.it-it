---
description: L'oggetto criterio viene utilizzato per controllare l'accesso al database dell'autorità di protezione locale (LSA) e contiene informazioni applicabili all'intero sistema o stabilisce impostazioni predefinite per il sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Oggetto Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878946"
---
# <a name="policy-object"></a>Oggetto Policy

L'oggetto **criterio** viene utilizzato per controllare l'accesso al database dell' [*autorità di protezione locale*](/windows/desktop/SecGloss/l-gly) (LSA) e contiene informazioni applicabili all'intero sistema o stabilisce impostazioni predefinite per il sistema. Ogni sistema dispone di un solo oggetto **criteri** . Questo oggetto **criterio** viene creato dall'LSA all'avvio del sistema e le applicazioni non possono crearlo o eliminarlo definitivamente.

Le informazioni archiviate in un oggetto **criteri** includono:

-   Quota di memoria predefinita del sistema. Se non diversamente specificato, a ogni utente che accede al sistema verrà assegnata questa quota di memoria. Le quote di memoria speciali possono essere assegnate a singoli utenti o membri di gruppi o gruppi locali tramite un oggetto [**account**](account-object.md) .
-   Requisiti di controllo di sicurezza a livello di sistema.
-   Nome e SID del dominio dell'account di questo sistema.
-   Informazioni sul dominio primario di questo sistema. Queste informazioni includono il nome e il SID del dominio primario, il nome dell'account nel dominio primario da usare per le richieste di autenticazione, il nome e le traduzioni SID e il recupero dei nomi dei controller di dominio all'interno del dominio. Questi nomi potrebbero non essere aggiornati e devono essere considerati solo come hint. Si presuppone che l'ordine di questo elenco sia significativo e venga mantenuto. Questo consente, ad esempio, il primo nome nell'elenco per rappresentare l'ultimo controller di dominio primario noto.
-   Informazioni che determinano se la LSA utilizza la copia master delle informazioni sui criteri o una replica. Solo una parte delle informazioni sui criteri viene replicata; il resto viene stabilito in base al sistema.

I campi **AccountDomain** e **PrimaryDomain** dell'oggetto **policy** vengono utilizzati per scopi diversi a seconda del tipo di relazioni di sistema e di trust:

-   In un sistema che non dispone di un dominio primario, il campo **AccountDomain** contiene il nome e il SID del dominio dell'account locale del sistema, che corrisponde al nome del computer. Il campo **PrimaryDomain** contiene il nome del gruppo di lavoro di cui è membro il computer. Gli oggetti [**trustedDomain**](trusteddomain-object.md) vengono ignorati con un'eccezione. non può essere presente un oggetto **trustedDomain** con lo stesso nome del gruppo di lavoro perché verrà visualizzato come se fosse il dominio primario del computer.
-   In un sistema che dispone di un dominio primario, il campo **AccountDomain** identifica il nome e il SID del dominio dell'account locale, come prima. Tuttavia, il campo **PrimaryDomain** contiene il nome e il SID del dominio primario per il sistema. Deve inoltre essere presente un oggetto [**trustedDomain**](trusteddomain-object.md) con il nome e il SID identificati nel campo **PrimaryDomain** . Questo oggetto **trustedDomain** contiene le informazioni relative all'account e al server necessarie per stabilire un canale sicuro per un controller di dominio nel dominio primario. Tutti gli altri oggetti **trustedDomain** vengono ignorati.
-   Nei controller di dominio il campo **AccountDomain** identifica il dominio dell'account locale per il sistema; il nome dell'account viene tuttavia assegnato dall'utente anziché essere un nome noto. Poiché il dominio primario è lo stesso del dominio dell'account, il campo **PrimaryDomain** deve contenere lo stesso valore del campo **AccountDomain** . Inoltre, è previsto che tutti gli oggetti [**trustedDomain**](trusteddomain-object.md) siano validi e rappresentino relazioni di trust con altri domini. Se il sistema non considera attendibili altri domini, non devono essere presenti oggetti **trustedDomain** .

 

 
