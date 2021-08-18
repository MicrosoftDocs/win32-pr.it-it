---
description: Illustra le parti del modello di controllo di accesso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Parti del modello di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785671"
---
# <a name="parts-of-the-access-control-model"></a>Parti del modello di controllo di accesso

Esistono due parti di base del modello di controllo di accesso:

-   [Token di accesso](access-tokens.md), che contengono informazioni su un utente connesso
-   [Descrittori di sicurezza](security-descriptors.md), che contengono le informazioni di sicurezza che proteggono un [oggetto a protezione diretta](securable-objects.md)

Quando un utente accede, il sistema [*autentica il*](/windows/desktop/SecGloss/a-gly) nome account e la password dell'utente. Se l'accesso ha esito positivo, il sistema crea un token di accesso. Ogni [*processo*](/windows/desktop/SecGloss/p-gly) eseguito per conto di questo utente avrà una copia di questo token di accesso. Il token di accesso [contiene gli identificatori di sicurezza](security-identifiers.md) che identificano l'account dell'utente e tutti gli account di gruppo a cui appartiene l'utente. Il token contiene anche un elenco dei [privilegi dell'utente](privileges.md) o dei gruppi dell'utente. Il sistema usa questo token per identificare l'utente associato quando un processo tenta di accedere a un oggetto a protezione diretta o di eseguire un'attività di amministrazione del sistema che richiede privilegi.

Quando viene creato un oggetto a protezione [](/windows/desktop/SecGloss/s-gly) diretta, il sistema gli assegna un descrittore di sicurezza che contiene le informazioni di sicurezza specificate dall'autore oppure le informazioni di sicurezza predefinite se non ne viene specificato nessuno. Le applicazioni possono usare funzioni per recuperare e impostare le informazioni di sicurezza per un oggetto esistente.

Un descrittore di sicurezza identifica il proprietario dell'oggetto e può contenere anche gli elenchi di controllo [di accesso seguenti:](access-control-lists.md)

-   Elenco [*di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) che identifica gli utenti e i gruppi autorizzati o negati all'oggetto
-   Elenco [*di controllo di accesso*](/windows/desktop/SecGloss/s-gly) di sistema (SACL) che controlla il modo in cui il sistema controlla [i](audit-generation.md) tentativi di accesso all'oggetto

Un ACL contiene un elenco di [voci di controllo di accesso](access-control-entries.md) (ACE). Ogni voce ACE specifica [](access-rights-and-access-masks.md) un set di diritti di [](trustees.md) accesso e contiene un SID che identifica un fiduciare per cui i diritti sono consentiti, negati o controllati. Un trustee può essere un account utente, un account di gruppo o una [*sessione di accesso.*](/windows/desktop/SecGloss/l-gly)

Usare le funzioni per modificare il contenuto di descrittori di sicurezza, SID e ACL anziché accedervi direttamente. Ciò consente di garantire che queste strutture rimangano sintatticamente accurate e impedisca ai miglioramenti futuri al sistema di sicurezza di interrompere il codice esistente.

Negli argomenti seguenti vengono fornite informazioni sulle parti del modello di controllo di accesso:

-   [Token di accesso](access-tokens.md)
-   [Descrittori di sicurezza](security-descriptors.md)
-   [Elenchi di controllo di accesso](access-control-lists.md)
-   [Voci di controllo di accesso](access-control-entries.md)
-   [Diritti di accesso e maschere di accesso](access-rights-and-access-masks.md)
-   [Funzionamento di AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Criteri di autorizzazione centralizzati](centralized-authorization-policy.md)
-   [Identificatori di sicurezza](security-identifiers.md)

 

 
