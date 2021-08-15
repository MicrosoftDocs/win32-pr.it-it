---
description: Sono disponibili diverse funzioni che recuperano informazioni sul controllo di accesso da un elenco di controllo di accesso (ACL).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Recupero di informazioni da un ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ef90d40058efd19790829f92c37a976359cbc61601d72fa2fee4cc4a93ec7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913673"
---
# <a name="getting-information-from-an-acl"></a>Recupero di informazioni da un ACL

Sono disponibili diverse funzioni che recuperano informazioni sul controllo di accesso da un elenco [*di controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACL). Sono incluse funzioni per determinare i diritti di accesso che un ACL concede o controlla per un [trustee specificato.](trustees.md) Altre funzioni consentono di estrarre informazioni sulle voci di [*controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACE) in un ACL.

La [**funzione GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera una matrice di strutture [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) che descrivono le voci ACE in un ACL. Ciò può essere utile quando si copiano informazioni ACE da un ACL a un altro. Ad esempio, una chiamata a **GetExplicitEntriesFromAcl** per ottenere informazioni sulle voci ACE in un ACL può essere seguita passando le strutture **EXPLICIT \_ ACCESS** restituite in una chiamata alla funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per creare ACE equivalenti in un nuovo ACL.

La [**funzione GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) consente di determinare i diritti di accesso effettivi che un dacl concede a un trustee specificato. I diritti di accesso effettivi del fiduciare sono i diritti di accesso che un dacl concede al fiduciare o a qualsiasi gruppo di cui il fiduciare è membro. **GetEffectiveRightsFromAcl** controlla tutte le ACE con accesso consentito e negato nell'elenco DACL specificato.

**Usare la procedura seguente per determinare i diritti di accesso di un trustee a un oggetto**

1.  Chiamare la [**funzione GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per ottenere un puntatore all'elenco DACL di un oggetto.
2.  Chiamare la [**funzione GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) per recuperare i diritti di accesso che l'elenco DACL concede a un trustee specificato.

La [**funzione GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) consente di controllare un elenco SACL per determinare i diritti di accesso controllati per un trustee specificato o per tutti i gruppi di cui il trustee è membro. I diritti controllati indicano i tipi di tentativi di accesso che causano la generazione di un record di controllo nel registro eventi di sicurezza da parte del sistema. La funzione restituisce due maschere [*di*](/windows/desktop/SecGloss/a-gly)accesso: una contenente i diritti di accesso monitorati per i tentativi di accesso non riusciti e l'altra contenente i diritti di accesso monitorati per l'accesso riuscito. **GetAuditedPermissionsFromAcl** controlla tutte le voci ACE di controllo di sistema in un ELENCO di controllo di accesso condiviso.

 

 
