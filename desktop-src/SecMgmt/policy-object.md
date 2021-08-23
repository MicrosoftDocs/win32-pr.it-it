---
description: L'oggetto Policy viene usato per controllare l'accesso al database dell'autorità di sicurezza locale (LSA) e contiene informazioni che si applicano all'intero sistema o stabiliscono le impostazioni predefinite per il sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Oggetto Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49e3dd7a33fd83107f9338783e3b8bdcc68eee7d8c4f927f67a7df1c0262c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005063"
---
# <a name="policy-object"></a>Oggetto Criteri

**L'oggetto** Policy viene usato per controllare l'accesso al database dell'autorità di sicurezza locale [](/windows/desktop/SecGloss/l-gly) (LSA) e contiene informazioni che si applicano all'intero sistema o stabiliscono le impostazioni predefinite per il sistema. Ogni sistema ha un solo **oggetto** Criteri. Questo **oggetto Criteri** viene creato dall'LSA all'avvio del sistema e le applicazioni non possono crearlo o eliminarlo.

Le informazioni archiviate in un **oggetto Criteri** includono:

-   Quota di memoria predefinita del sistema. Se non diversamente specificato, a ogni utente che accede al sistema verrà assegnata questa quota di memoria. Le quote di memoria speciali possono essere assegnate a singoli utenti o membri di gruppi o gruppi locali tramite un [**oggetto Account.**](account-object.md)
-   Requisiti di controllo della sicurezza a livello di sistema.
-   Nome e SID del dominio dell'account di questo sistema.
-   Informazioni sul dominio primario di questo sistema. Queste informazioni includono il nome e il SID del dominio primario, il nome dell'account all'interno del dominio primario da usare per le richieste di autenticazione, le traduzioni di nome e SID e l'ottenimento dei nomi dei controller di dominio all'interno del dominio. Questi nomi possono non essere aggiornati e devono essere presi solo come suggerimento. Si presuppone che l'ordine di questo elenco sia significativo e verrà mantenuto. In questo modo, ad esempio, il nome nell'elenco rappresenta l'ultimo controller di dominio primario noto.
-   Informazioni sulla conservazione della copia master delle informazioni sui criteri o su una replica da parte dell'LSA. Viene replicata solo una parte delle informazioni sui criteri. il resto viene stabilito in base al sistema.

I **campi AccountDomain** **e PrimaryDomain** dell'oggetto **Policy** vengono usati per scopi diversi a seconda del tipo di relazioni di sistema e trust:

-   In un sistema che non dispone di un dominio primario, il campo **AccountDomain** contiene il nome e il SID del dominio dell'account locale del sistema, che corrisponde al nome del computer. Il **campo PrimaryDomain** contiene il nome del gruppo di lavoro di cui è membro il computer. [**Gli oggetti TrustedDomain**](trusteddomain-object.md) vengono ignorati con un'eccezione. Non può essere presente un oggetto **TrustedDomain** con lo stesso nome del gruppo di lavoro perché verrà visualizzato come se fosse il dominio primario del computer.
-   In un sistema con un dominio primario, il campo **AccountDomain** identifica il nome e il SID del dominio dell'account locale, come in precedenza. Tuttavia, il **campo PrimaryDomain** contiene il nome e il SID del dominio primario per il sistema. Inoltre, deve essere presente un [**oggetto TrustedDomain**](trusteddomain-object.md) con il nome e il SID identificati nel **campo PrimaryDomain.** Questo **oggetto TrustedDomain** contiene le informazioni sull'account e sul server necessarie per stabilire un canale sicuro per un controller di dominio nel dominio primario. Tutti gli **altri oggetti TrustedDomain** vengono ignorati.
-   Nei controller di dominio il **campo AccountDomain** identifica il dominio dell'account locale per il sistema. Tuttavia, il nome dell'account viene assegnato dall'utente anziché essere un nome noto. Poiché il dominio primario è lo stesso del dominio dell'account, il **campo PrimaryDomain** deve contenere lo stesso valore del **campo AccountDomain.** Si prevede inoltre che tutti gli oggetti [**TrustedDomain**](trusteddomain-object.md) siano validi e rappresentino relazioni di trust con altri domini. Se il sistema non considera attendibili altri domini, non devono essere presenti **oggetti TrustedDomain.**

 

 
