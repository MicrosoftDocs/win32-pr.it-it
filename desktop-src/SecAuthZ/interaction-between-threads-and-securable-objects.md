---
description: In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel token di accesso dei thread con le informazioni di sicurezza nel descrittore di sicurezza degli oggetti.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interazione tra thread e oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670817"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interazione tra thread e oggetti a protezione diretta

Quando un thread tenta di usare un oggetto a [protezione](securable-objects.md)diretta, il sistema esegue un controllo di accesso prima di consentire al thread di continuare. In un controllo di accesso, il sistema confronta le informazioni di sicurezza nel [*token*](/windows/desktop/SecGloss/a-gly) di accesso del thread con le informazioni di sicurezza nel descrittore di sicurezza [*dell'oggetto*](/windows/desktop/SecGloss/s-gly).

-   Il token di accesso [*contiene gli identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identificano l'utente associato al thread.
-   Il descrittore di sicurezza identifica il proprietario dell'oggetto e contiene un elenco di controllo di [*accesso*](/windows/desktop/SecGloss/d-gly) discrezionale (DACL). L'elenco DACL contiene [*voci*](/windows/desktop/SecGloss/a-gly) di controllo di accesso (ACE), ognuna delle quali specifica i diritti di accesso consentiti o negati a un utente o a un gruppo specifico.

Il sistema controlla l'elenco DACL dell'oggetto, cercando le voci ACE applicabili ai SID dell'utente e del gruppo dal token di accesso del thread. Il sistema controlla ogni ACE fino a quando l'accesso non viene concesso o negato o finché non sono presenti altre voci ACE da controllare. È possibile che un elenco di [*controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACL) abbia diverse ACE applicabili ai SID del token. E, in questo caso, si accumulano i diritti di accesso concessi da ogni ACE. Ad esempio, se una ACE concede l'accesso in lettura a un gruppo e un'altra ACE concede l'accesso in scrittura a un utente membro del gruppo, l'utente può avere sia l'accesso in lettura che in scrittura all'oggetto.

La figura seguente illustra la relazione tra questi blocchi di informazioni di sicurezza:

![relazioni tra processi, assi e dacl](images/cssec-02.png)

 

 
