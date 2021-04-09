---
description: Windows supporta un set di funzioni che creano un elenco di controllo di accesso (ACL) o modificano le voci di controllo di accesso (ACE) in un ACL esistente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Creazione o modifica di un ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879890"
---
# <a name="creating-or-modifying-an-acl"></a>Creazione o modifica di un ACL

Windows supporta un set di funzioni che creano un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) o modificano le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) in un ACL esistente.

La funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) crea un nuovo ACL. **SetEntriesInAcl** può specificare un set completamente nuovo di ACE per l'ACL oppure può unire una o più nuove voci ACE con le voci ACE di un ACL esistente. La funzione **SetEntriesInAcl** usa una matrice di strutture di [**\_ accesso esplicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) per specificare le informazioni per le nuove voci ACE. Ogni struttura di **\_ accesso esplicita** contiene informazioni che descrivono una singola voce ACE. Queste informazioni includono i diritti di accesso, il tipo di ACE, i flag che controllano l'ereditarietà ACE e una struttura [**trustee**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) che identifica il trustee.

**Per aggiungere una nuova voce ACE a un ACL esistente**

1.  Utilizzare la funzione [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere l'elenco DACL o SACL esistente dal [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto.
2.  Per ogni nuova voce ACE, chiamare la funzione [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) per riempire una struttura di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con le informazioni che descrivono la voce ACE.
3.  Chiamare [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), specificando l'ACL esistente e una matrice di strutture di [**\_ accesso esplicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) per le nuove voci ACE. La funzione **SetEntriesInAcl** alloca e Inizializza l'ACL e le relative voci ACE.
4.  Chiamare la funzione [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per allegare il nuovo ACL al descrittore di sicurezza dell'oggetto.

Se il chiamante specifica un ACL esistente, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) unisce le nuove informazioni ACE con le voci ACE esistenti nell'ACL. Si consideri, ad esempio, il caso in cui l'ACL esistente concede l'accesso a un trustee specificato e una struttura di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) nega l'accesso allo stesso trustee. In questo caso, **SetEntriesInAcl** aggiunge una nuova voce ACE di accesso negato per il trustee ed Elimina o modifica l'ACE esistente consentito per l'accesso al trustee.

Per il codice di esempio che unisce una nuova voce ACE in un ACL esistente, vedere [modifica degli ACL di un oggetto in C++](modifying-the-acls-of-an-object-in-c--.md).

 

 
