---
description: Windows supporta un set di funzioni che creano un elenco di controllo di accesso (ACL) o modificano le voci di controllo di accesso (ACE) in un ACL esistente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Creazione o modifica di un elenco di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120b445d37f8c4b82c2b0b2a775a06d68faa46ab5752cc25e913d43676e9a72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782166"
---
# <a name="creating-or-modifying-an-acl"></a>Creazione o modifica di un elenco di controllo di accesso

Windows supporta un set di funzioni che [](/windows/desktop/SecGloss/a-gly) creano un elenco di controllo di accesso (ACL) o modificano le voci di controllo [*di*](/windows/desktop/SecGloss/a-gly) accesso (ACE) in un ACL esistente.

La [**funzione SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) crea un nuovo ACL. **SetEntriesInAcl** può specificare un set completamente nuovo di voci di controllo di accesso per l'ACL oppure può unire una o più nuove voci di controllo di accesso con le ACE di un ACL esistente. La **funzione SetEntriesInAcl** usa una matrice di [**strutture EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) per specificare le informazioni per le nuove voci ACE. Ogni **struttura EXPLICIT \_ ACCESS** contiene informazioni che descrivono una singola ACE. Queste informazioni includono i diritti di accesso, il tipo di ACE, i flag che controllano l'ereditarietà ACE e una struttura [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) che identifica il fiduciare.

**Per aggiungere una nuova ACE a un elenco di controllo di accesso esistente**

1.  Usare la [**funzione GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere l'elenco DACL o SACL esistente dal descrittore di sicurezza [*di un oggetto*](/windows/desktop/SecGloss/s-gly).
2.  Per ogni nuova ACE, chiamare la [**funzione BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) per riempire una struttura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con le informazioni che descrivono la ACE.
3.  Chiamare [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), specificando l'ACL esistente e una matrice di strutture [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) per le nuove ACE. La **funzione SetEntriesInAcl** alloca e inizializza l'ACL e le relative voci ACE.
4.  Chiamare la [**funzione SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per collegare il nuovo ACL al descrittore di sicurezza dell'oggetto.

Se il chiamante specifica un ACL esistente, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) unisce le nuove informazioni ACE alle voci ACE esistenti nell'ACL. Si consideri il caso, ad esempio, in cui l'elenco di controllo di accesso esistente concede l'accesso a un fiduciare specificato e una struttura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) nega l'accesso allo stesso fiduciare. In questo caso, **SetEntriesInAcl** aggiunge una nuova voce ACE negata di accesso per il trustee ed elimina o modifica la voce ACE esistente consentita per il trustee.

Per codice di esempio che unisce una nuova ACE in un ACL esistente, vedere Modifica degli ACL di un oggetto [in C++.](modifying-the-acls-of-an-object-in-c--.md)

 

 
