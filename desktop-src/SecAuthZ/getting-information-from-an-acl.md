---
description: Sono disponibili diverse funzioni che recuperano le informazioni di controllo di accesso da un elenco di controllo di accesso (ACL).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Recupero di informazioni da un ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f87aebc2bc9b05191b5026b990714c2519091be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233262"
---
# <a name="getting-information-from-an-acl"></a>Recupero di informazioni da un ACL

Sono disponibili diverse funzioni che recuperano le informazioni di controllo di accesso da un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL). Queste includono funzioni che consentono di determinare i diritti di accesso concessi o controlli da un ACL per un [trustee](trustees.md)specificato. Altre funzioni consentono di estrarre informazioni sulle voci di [*controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) in un ACL.

La funzione [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera una matrice di strutture di [**\_ accesso esplicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) che descrivono le voci ACE in un ACL. Questa operazione può essere utile quando si copiano le informazioni ACE da un ACL a un altro. Ad esempio, una chiamata a **GetExplicitEntriesFromAcl** per ottenere informazioni sulle voci ACE in un ACL può essere seguita passando le strutture di **\_ accesso esplicite** restituite in una chiamata alla funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per creare Ace equivalenti in un nuovo ACL.

La funzione [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) consente di determinare i diritti di accesso validi che un DACL concede a un trustee specificato. I diritti di accesso validi del trustee sono i diritti di accesso concessi da un DACL al trustee o a tutti i gruppi di cui il trustee è membro. **GetEffectiveRightsFromAcl** controlla tutte le voci di accesso consentito e accesso negato nell'elenco DACL specificato.

**Usare la procedura seguente per determinare i diritti di accesso di un trustee a un oggetto**

1.  Chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere un puntatore all'elenco DACL di un oggetto.
2.  Chiamare la funzione [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) per recuperare i diritti di accesso concessi dal DACL a un trustee specificato.

La funzione [**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) consente di controllare un SACL per determinare i diritti di accesso controllati per un trustee specificato o per tutti i gruppi di cui il trustee è membro. I diritti controllati indicano i tipi di tentativi di accesso che determinano la generazione di un record di controllo nel registro eventi di sicurezza da parte del sistema. La funzione restituisce due [*maschere di accesso*](/windows/desktop/SecGloss/a-gly): una contenente i diritti di accesso monitorati per i tentativi di accesso non riusciti e l'altra contenente i diritti di accesso monitorati per l'accesso riuscito. **GetAuditedPermissionsFromAcl** controlla tutte le voci di controllo di sistema in un SACL.

 

 
