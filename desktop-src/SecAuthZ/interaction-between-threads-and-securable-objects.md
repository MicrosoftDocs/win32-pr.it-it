---
description: In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel token di accesso dei thread con le informazioni di sicurezza nel descrittore di sicurezza degli oggetti.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interazione tra thread e oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884453"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interazione tra thread e oggetti a protezione diretta

Quando un thread tenta di utilizzare un [oggetto a protezione diretta](securable-objects.md), il sistema esegue un controllo di accesso prima di consentire al thread di proseguire. In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel token di [*accesso*](/windows/desktop/SecGloss/a-gly) del thread con le informazioni di sicurezza nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto.

-   Il token di accesso contiene gli [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identificano l'utente associato al thread.
-   Il descrittore di sicurezza identifica il proprietario dell'oggetto e contiene un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL). Il DACL contiene le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE), ognuna delle quali specifica i diritti di accesso consentiti o negati a un utente o a un gruppo specifico.

Il sistema controlla l'elenco DACL dell'oggetto, cercando le voci ACE che si applicano ai SID utente e gruppo dal token di accesso del thread. Il sistema controlla ogni voce ACE fino a quando l'accesso non viene concesso o negato o fino a quando non sono presenti altre voci ACE da verificare. In teoria, un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) potrebbe avere diverse voci ACE applicabili ai SID del token. E, in questo caso, i diritti di accesso concessi da ogni ACE si accumulano. Se ad esempio una voce ACE concede l'accesso in lettura a un gruppo e un'altra voce ACE concede l'accesso in scrittura a un utente che è membro del gruppo, l'utente può disporre di accesso in lettura e scrittura all'oggetto.

Nella figura seguente viene illustrata la relazione tra questi blocchi di informazioni di sicurezza:

![relazioni tra processi, ACE e DACL](images/cssec-02.png)

 

 
