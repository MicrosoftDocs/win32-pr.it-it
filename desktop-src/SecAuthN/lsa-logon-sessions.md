---
description: Una sessione di accesso è una sessione di elaborazione che inizia quando l'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessioni di accesso LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232833"
---
# <a name="lsa-logon-sessions"></a>Sessioni di accesso LSA

Una [*sessione di accesso*](../secgloss/l-gly.md) è una sessione di elaborazione che inizia quando l'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.

Quando un utente viene autenticato correttamente, il pacchetto di autenticazione crea una sessione di accesso e restituisce informazioni all' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) utilizzata per creare un [*token*](../secgloss/t-gly.md) per il nuovo utente. Questo token include, tra le altre cose, un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) per la sessione di accesso, denominato [*ID di accesso*](../secgloss/l-gly.md).

Quando viene creato un token, il [*conteggio dei riferimenti*](../secgloss/r-gly.md) per la sessione di accesso viene incrementato. Il conteggio dei riferimenti viene incrementato anche ogni volta che vengono create copie del token per la creazione, la rappresentazione o altri usi del processo. Quando vengono completati i token utilizzati e le copie del token vengono eliminate, il conteggio dei riferimenti per la sessione di accesso viene decrementato. Quando il conteggio dei riferimenti raggiunge zero, la sessione di accesso viene eliminata.

> [!Note]  
> Se l'autenticazione ha esito negativo, il [*pacchetto di autenticazione*](../secgloss/a-gly.md) non deve creare una sessione di accesso. Se il pacchetto di autenticazione deve creare una sessione di accesso prima di prendere una decisione finale sulla validità dell'utente e se l'autenticazione ha esito negativo, il pacchetto di autenticazione deve eliminare la sessione.

 

 

 
