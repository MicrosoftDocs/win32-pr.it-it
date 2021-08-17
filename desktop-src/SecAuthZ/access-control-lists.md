---
description: Un elenco di controllo di accesso (ACL) è un elenco di voci di controllo di accesso (ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Elenchi di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7021767830dead84f2ea965c46ca205257a2f18443f352ec85becc0139e30e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785661"
---
# <a name="access-control-lists"></a>Elenchi di controllo di accesso

Un [*elenco di controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACL) è un elenco di voci di controllo di [accesso](access-control-entries.md) (ACE). Ogni voce dell'elenco di controllo di accesso identifica un [elemento trusted](trustees.md) e specifica i [diritti di accesso](access-rights-and-access-masks.md) concessi, negati o controllati per l'elemento trusted stesso. Il [descrittore di sicurezza](security-descriptors.md) per un oggetto a protezione [diretta](securable-objects.md) può contenere due tipi di ACL: un DACL e un SACL.

Un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/d-gly) discrezionale (DACL) identifica i trustee a cui è consentito o negato l'accesso a un oggetto a protezione diretta. Quando un [*processo tenta*](/windows/desktop/SecGloss/p-gly) di accedere a un oggetto a protezione diretta, il sistema controlla le voci ACE nell'elenco DACL dell'oggetto per determinare se concedere l'accesso. Se l'oggetto non dispone di un elenco DACL, il sistema concede l'accesso completo a tutti gli utenti. Se l'elenco DACL dell'oggetto non dispone di ACE, il sistema nega tutti i tentativi di accesso all'oggetto perché l'elenco DACL non consente diritti di accesso. Il sistema controlla le ACE in sequenza finché non trova una o più ACE che consentono tutti i diritti di accesso richiesti o fino a quando non viene negato uno dei diritti di accesso richiesti. Per altre informazioni, vedere [Controllo DACL dell'accesso a un oggetto](how-dacls-control-access-to-an-object.md). Per informazioni su come creare correttamente un dacl, vedere [Creazione di un dacl.](/windows/desktop/SecBP/creating-a-dacl)

Un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/s-gly) di sistema (SACL) consente agli amministratori di registrare i tentativi di accesso a un oggetto protetto. Ogni voce ACE specifica i tipi di tentativi di accesso da parte di un trustee specificato che determinano la generazione di un record nel registro eventi di sicurezza da parte del sistema. Una voce ACE in un elenco SACL può generare record di controllo quando un tentativo di accesso ha esito negativo, quando ha esito positivo o entrambi. Per altre informazioni sugli ACL, vedere [Audit Generation and](audit-generation.md) [SACL Access Right](sacl-access-right.md).

Non tentare di usare direttamente il contenuto di un ACL. Per assicurarsi che gli ACL siano semanticamente corretti, usare le funzioni appropriate per creare e modificare gli ACL. Per altre informazioni, vedere [Recupero di informazioni da un ACL](getting-information-from-an-acl.md) e Creazione o modifica di un [ACL.](creating-or-modifying-an-acl.md)

Gli ACL forniscono anche il controllo di accesso agli oggetti del servizio directory Microsoft Active Directory. Active Directory Service Interfaces (ADSI) include routine per creare e modificare il contenuto di questi ACL. Per altre informazioni, vedere [Controllo dell'accesso agli oggetti di Active Directory.](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services)

 

 
