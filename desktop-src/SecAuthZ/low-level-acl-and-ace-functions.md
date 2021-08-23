---
description: Creare un elenco di controllo di accesso (ACL) usando le funzioni di basso livello, allocare un buffer per l'elenco di controllo di accesso e quindi inizializzarlo chiamando la funzione InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Funzioni ACL e ACE di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab8c968c19e652f530abe25aaae11e47f36db1cd6ea7184120987c63a1bd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670661"
---
# <a name="low-level-acl-and-ace-functions"></a>Funzioni ACL e ACE di basso livello

Per creare un elenco [*di controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACL) usando le funzioni di basso livello, allocare un buffer per l'elenco di controllo di accesso e quindi inizializzarlo chiamando la [**funzione InitializeAcl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) Per aggiungere voci di [*controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACE) alla fine di un elenco di controllo di accesso discrezionale (DACL), usare le [**funzioni AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAccessDeniedAce.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) [](/windows/desktop/SecGloss/d-gly) La [**funzione AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) aggiunge una voce ACE alla fine di [*un*](/windows/desktop/SecGloss/s-gly) elenco di controllo di accesso di sistema (SACL). È possibile usare la [**funzione AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) per aggiungere una o più ACE in una posizione specificata in un ACL. La **funzione AddAce** consente anche di aggiungere una ACE ereditabile a un elenco di controllo di accesso. La [**funzione DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) rimuove una ACE da una posizione specificata in un elenco di controllo di accesso. La [**funzione GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) recupera una ACE da una posizione specificata in un ACL. La [**funzione FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) recupera un puntatore al primo byte disponibile in un ACL.

Per modificare un elenco di controllo di accesso esistente nel descrittore di sicurezza di un [*oggetto,*](/windows/desktop/SecGloss/s-gly)usare la [**funzione GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) o [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) per ottenere l'ACL esistente. È possibile usare la [**funzione GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) per copiare le voci di controllo di accesso dall'elenco di controllo di accesso esistente. Dopo l'allocazione e l'inizializzazione di un nuovo ACL, usare funzioni come [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) per aggiungerne le voci ACE. Al termine della compilazione del nuovo ACL, usare la [**funzione SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) o [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) per aggiungere il nuovo ACL al descrittore di sicurezza dell'oggetto.

È possibile usare le funzioni [**AddAccessAllowedObjectAce,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)o [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) per aggiungere ACE specifiche dell'oggetto alla fine di un ACL. [](object-specific-aces.md)

 

 
