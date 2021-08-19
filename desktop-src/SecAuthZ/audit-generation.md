---
description: I requisiti di sicurezza a livello di C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generazione di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb2c6ab4b43d169e1ca6f6317489921987d22b507489ef0a5fd289d8483c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784697"
---
# <a name="audit-generation"></a>Generazione di controllo

I requisiti di sicurezza a livello di C2 specificano che gli amministratori di sistema devono essere in grado di controllare gli eventi correlati alla sicurezza e che l'accesso a questi dati di controllo deve essere limitato agli amministratori autorizzati. L Windows API fornisce funzioni che consentono a un amministratore di monitorare gli eventi correlati alla sicurezza.

Il descrittore di sicurezza per un oggetto a protezione diretta può avere un elenco di [*controllo*](/windows/desktop/SecGloss/s-gly) di accesso di sistema (SACL). Un sacl contiene [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) che specificano i tipi di tentativi di accesso che generano report di controllo. Ogni voce ACE identifica un trustee, un set di diritti di accesso e un set di flag che indicano se il sistema genera messaggi di controllo per tentativi di accesso non riusciti, tentativi di accesso riusciti o entrambi.

Il sistema scrive i messaggi di controllo nel registro eventi di sicurezza. Per informazioni sull'accesso ai record in un registro eventi di sicurezza, vedere [Registrazione eventi](/windows/desktop/EventLog/event-logging).

Per leggere o scrivere l'elenco SACL di un oggetto, un thread deve prima abilitare il edizione Standard \_ SECURITY \_ NAME. Per altre informazioni, vedere [Diritto di accesso SACL.](sacl-access-right.md)

L Windows API fornisce anche il supporto per le applicazioni server per generare messaggi di controllo quando un client tenta di accedere a un oggetto privato. Per altre informazioni, vedere [Controllo dell'accesso a oggetti privati.](auditing-access-to-private-objects.md)

 

 
