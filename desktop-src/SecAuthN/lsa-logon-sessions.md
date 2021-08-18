---
description: Una sessione di accesso è una sessione di calcolo che inizia quando un'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessioni di accesso LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4bc6adc81b22b0e48a83b8aec4f9130b1fcb906bea5078afc6517563c98b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922326"
---
# <a name="lsa-logon-sessions"></a>Sessioni di accesso LSA

Una [*sessione di accesso*](../secgloss/l-gly.md) è una sessione di calcolo che inizia quando un'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.

Quando un utente viene autenticato correttamente, il pacchetto di [](../secgloss/l-gly.md) autenticazione crea una sessione di accesso e restituisce informazioni all'autorità di sicurezza locale (LSA) usata per creare un [*token*](../secgloss/t-gly.md) per il nuovo utente. Questo token include, tra le altre cose, un identificatore [*univoco*](../secgloss/l-gly.md) locale (LUID) per la sessione di accesso, denominato [*ID di accesso*](../secgloss/l-gly.md).

Quando viene creato un token, il [*conteggio dei riferimenti*](../secgloss/r-gly.md) per la sessione di accesso viene incrementato. Il conteggio dei riferimenti viene incrementato anche ogni volta che vengono create copie del token per la creazione, la rappresentazione o altri usi del processo. Quando gli usi del token vengono completati e le copie del token vengono eliminate, il conteggio dei riferimenti per la sessione di accesso viene decrementato. Quando il conteggio dei riferimenti raggiunge lo zero, la sessione di accesso viene eliminata.

> [!Note]  
> Se l'autenticazione non riesce, il [*pacchetto di autenticazione*](../secgloss/a-gly.md) non deve creare una sessione di accesso. Se il pacchetto di autenticazione deve creare una sessione di accesso prima di determinare definitivamente la validità dell'utente e se l'autenticazione ha esito negativo, il pacchetto di autenticazione deve eliminare la sessione.

 

 

 
