---
description: I requisiti di sicurezza a livello C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generazione di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318254"
---
# <a name="audit-generation"></a>Generazione di controllo

I requisiti di sicurezza a livello C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati. L'API Windows fornisce funzioni che consentono a un amministratore di monitorare gli eventi correlati alla sicurezza.

Il descrittore di sicurezza per un oggetto a protezione diretta può avere un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Un SACL contiene [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) che specificano i tipi di tentativi di accesso che generano report di controllo. Ogni voce ACE identifica un trustee, un set di diritti di accesso e un set di flag che indicano se il sistema genera messaggi di controllo per tentativi di accesso non riusciti, tentativi di accesso riusciti o entrambi.

Il sistema scrive i messaggi di controllo nel registro eventi di sicurezza. Per informazioni sull'accesso ai record in un registro eventi di protezione, vedere [registrazione degli eventi](/windows/desktop/EventLog/event-logging).

Per leggere o scrivere il SACL di un oggetto, un thread deve prima abilitare il \_ \_ privilegio se nome sicurezza. Per ulteriori informazioni, vedere il [diritto di accesso SACL](sacl-access-right.md).

L'API Windows fornisce inoltre supporto per le applicazioni server per generare messaggi di controllo quando un client tenta di accedere a un oggetto privato. Per altre informazioni, vedere [controllo dell'accesso a oggetti privati](auditing-access-to-private-objects.md).

 

 
