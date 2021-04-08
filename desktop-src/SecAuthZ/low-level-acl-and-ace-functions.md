---
description: Creare un elenco di controllo di accesso (ACL) usando le funzioni di basso livello, allocare un buffer per l'ACL e quindi inizializzarlo chiamando la funzione InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Funzioni ACL e ACE di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884449"
---
# <a name="low-level-acl-and-ace-functions"></a>Funzioni ACL e ACE di basso livello

Per creare un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) utilizzando le funzioni di basso livello, allocare un buffer per l'ACL e quindi inizializzarlo chiamando la funzione [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) . Per aggiungere [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) alla fine di un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL), usare le funzioni [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAccessDeniedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . La funzione [**AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) aggiunge una voce ACE alla fine di un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). È possibile usare la funzione [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) per aggiungere una o più voci ACE in una posizione specificata in un ACL. La funzione **AddAce** consente inoltre di aggiungere una voce ACE ereditabile a un ACL. La funzione [**DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) rimuove una voce ACE da una posizione specificata in un ACL. La funzione [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) recupera una voce ACE da una posizione specificata in un ACL. La funzione [**FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) recupera un puntatore al primo byte libero in un ACL.

Per modificare un ACL esistente nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto, usare la funzione [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) o [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) per ottenere l'ACL esistente. È possibile usare la funzione [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) per copiare le voci ACE dall'ACL esistente. Dopo l'allocazione e l'inizializzazione di un nuovo ACL, usare funzioni quali [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) per aggiungere voci ACE. Al termine della compilazione del nuovo ACL, usare la funzione [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) o [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) per aggiungere il nuovo ACL al descrittore di sicurezza dell'oggetto.

È possibile usare le funzioni [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)o [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) per aggiungere [voci ACE specifiche dell'oggetto](object-specific-aces.md) alla fine di un ACL.

 

 
