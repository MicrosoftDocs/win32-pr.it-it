---
description: Illustra le parti del modello di controllo di accesso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Parti del modello di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3aa6d3547d486c33f4b31cdb5d5de24c7d27cec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881021"
---
# <a name="parts-of-the-access-control-model"></a>Parti del modello di controllo di accesso

Sono disponibili due parti di base del modello di controllo di accesso:

-   [Token di accesso](access-tokens.md), che contengono informazioni su un utente connesso
-   [Descrittori di sicurezza](security-descriptors.md), che contengono le informazioni di sicurezza che proteggono un [oggetto a protezione diretta](securable-objects.md)

Quando un utente esegue l'accesso, il sistema [*autentica*](/windows/desktop/SecGloss/a-gly) il nome e la password dell'account utente. Se l'accesso ha esito positivo, il sistema crea un token di accesso. Ogni [*processo*](/windows/desktop/SecGloss/p-gly) eseguito per conto di questo utente avrà una copia di questo token di accesso. Il token di accesso contiene gli [identificatori di sicurezza](security-identifiers.md) che identificano l'account dell'utente e gli account di gruppo a cui appartiene l'utente. Il token contiene anche un elenco dei [privilegi](privileges.md) utilizzati dall'utente o dai gruppi dell'utente. Questo token viene utilizzato dal sistema per identificare l'utente associato quando un processo tenta di accedere a un oggetto a protezione diretta o di eseguire un'attività di amministrazione del sistema che richiede privilegi.

Quando viene creato un oggetto a protezione diretta, il sistema lo assegna a un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) che contiene le informazioni di sicurezza specificate dal creatore oppure le informazioni di sicurezza predefinite se non ne viene specificato alcuno. Le applicazioni possono utilizzare le funzioni per recuperare e impostare le informazioni di sicurezza per un oggetto esistente.

Un descrittore di sicurezza identifica il proprietario dell'oggetto e può anche contenere gli [elenchi di controllo di accesso](access-control-lists.md)seguenti:

-   [*Elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) che identifica gli utenti e i gruppi a cui è consentito o negato l'accesso all'oggetto
-   Un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) che controlla il modo in cui il sistema controlla [i tentativi di](audit-generation.md) accesso all'oggetto

Un ACL contiene un elenco di [voci di controllo di accesso](access-control-entries.md) (ACE). Ogni voce ACE specifica un set di [diritti di accesso](access-rights-and-access-masks.md) e contiene un SID che identifica un [trustee](trustees.md) per il quale i diritti sono consentiti, negati o controllati. Un trustee può essere un account utente, un account di gruppo o una [*sessione di accesso*](/windows/desktop/SecGloss/l-gly).

Usare le funzioni per modificare il contenuto dei descrittori di sicurezza, dei SID e degli ACL anziché accedervi direttamente. Ciò garantisce che queste strutture rimangano sintatticamente accurate e impediscano ai futuri miglioramenti al sistema di sicurezza di suddividere il codice esistente.

Negli argomenti seguenti vengono fornite informazioni sulle parti del modello di controllo di accesso:

-   [Token di accesso](access-tokens.md)
-   [Descrittori di sicurezza](security-descriptors.md)
-   [Elenchi di controllo di accesso](access-control-lists.md)
-   [Voci di controllo di accesso](access-control-entries.md)
-   [Maschere di accesso e diritti di accesso](access-rights-and-access-masks.md)
-   [Funzionamento di AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Criteri di autorizzazione centralizzati](centralized-authorization-policy.md)
-   [ID di sicurezza](security-identifiers.md)

 

 
