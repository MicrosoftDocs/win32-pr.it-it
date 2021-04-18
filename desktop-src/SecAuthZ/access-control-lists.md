---
description: Un elenco di controllo di accesso (ACL) è un elenco di voci di controllo di accesso (ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Elenchi di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a788f02f8a04711be7db8268833375b2519d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310954"
---
# <a name="access-control-lists"></a>Elenchi di controllo di accesso

Un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) è un elenco di [voci di controllo di accesso](access-control-entries.md) (ACE). Ogni voce dell'elenco di controllo di accesso identifica un [elemento trusted](trustees.md) e specifica i [diritti di accesso](access-rights-and-access-masks.md) concessi, negati o controllati per l'elemento trusted stesso. Il [descrittore di sicurezza](security-descriptors.md) per un [oggetto a protezione diretta](securable-objects.md) può contenere due tipi di ACL: un DACL e un SACL.

Un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) identifica i trustee a cui è consentito o negato l'accesso a un oggetto a protezione diretta. Quando un [*processo*](/windows/desktop/SecGloss/p-gly) tenta di accedere a un oggetto a protezione diretta, il sistema controlla le voci ACE nell'elenco DACL dell'oggetto per determinare se concederne l'accesso. Se l'oggetto non dispone di un DACL, il sistema concede l'accesso completo a tutti gli utenti. Se il DACL dell'oggetto non dispone di voci ACE, il sistema nega tutti i tentativi di accesso all'oggetto perché l'elenco DACL non consente diritti di accesso. Il sistema controlla le voci ACE in sequenza fino a trovare una o più voci ACE che consentono tutti i diritti di accesso richiesti o fino a quando non viene negato alcuno dei diritti di accesso richiesti. Per ulteriori informazioni, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md). Per informazioni su come creare correttamente un DACL, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).

Un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) consente agli amministratori di registrare i tentativi di accesso a un oggetto protetto. Ogni voce ACE specifica i tipi di tentativi di accesso da parte di un trustee specificato che determina la generazione di un record nel registro eventi di sicurezza da parte del sistema. Una voce ACE in un SACL può generare record di controllo quando un tentativo di accesso ha esito negativo, quando ha esito positivo o entrambi. Per ulteriori informazioni sui SACL, vedere la pagina relativa alla [generazione di controlli](audit-generation.md) e [al diritto di accesso SACL](sacl-access-right.md).

Non tentare di utilizzare direttamente il contenuto di un ACL. Per assicurarsi che gli ACL siano semanticamente corretti, usare le funzioni appropriate per creare e modificare gli ACL. Per ulteriori informazioni, vedere [recupero di informazioni da un ACL](getting-information-from-an-acl.md) e [creazione o modifica di un ACL](creating-or-modifying-an-acl.md).

Gli ACL forniscono inoltre il controllo di accesso agli oggetti del servizio directory Microsoft Active Directory. Le interfacce ADSI (Active Directory Service Interfaces) includono routine per la creazione e la modifica del contenuto di questi ACL. Per altre informazioni, vedere [controllo dell'accesso agli oggetti Active Directory](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services).

 

 
