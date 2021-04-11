---
description: Microsoft fornisce il \_ pacchetto di autenticazione MSV1 0 per gli accessi al computer locale che non richiedono l'autenticazione personalizzata.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: Pacchetto di autenticazione MSV1_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232827"
---
# <a name="msv1_0-authentication-package"></a>\_Pacchetto di autenticazione MSV1 0

Microsoft fornisce il \_ pacchetto di [*autenticazione*](../secgloss/a-gly.md) MSV1 0 per gli accessi al computer locale che non richiedono l'autenticazione personalizzata. L' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) chiama il \_ pacchetto di autenticazione MSV1 0 per elaborare i dati di accesso raccolti da [*Gina*](../secgloss/g-gly.md) per il processo di accesso [*Winlogon*](../secgloss/w-gly.md) . Il \_ pacchetto MSV1 0 controlla il database di gestione degli account di sicurezza (Sam) locale per determinare se i dati di accesso appartengono a un' [*entità di sicurezza*](../secgloss/s-gly.md) valida e quindi restituisce il risultato del tentativo di accesso all'LSA.

MSV1 \_ 0 supporta anche gli accessi al dominio. MSV1 \_ 0 elabora gli accessi al dominio usando l'autenticazione pass-through, come illustrato nella figura seguente.

![\-pacchetto di autenticazione MSV1 0](images/lsaint4.png)

Nell'autenticazione pass-through, l'istanza locale di MSV1 \_ 0 usa il servizio Netlogon per chiamare l'istanza di MSV1 \_ 0 in esecuzione sul controller di dominio. L'istanza del controller di dominio di MSV1 \_ 0 controlla quindi il database SAM del controller di dominio e restituisce il risultato dell'accesso all'istanza di MSV1 \_ 0 nel computer locale. La versione locale di MSV1 \_ 0 invia il risultato dell'accesso all'istanza di LSA nel computer locale.

Se il controller di dominio non è disponibile e l'LSA contiene [*credenziali*](../secgloss/c-gly.md) memorizzate nella cache per l'utente, l'istanza locale di MSV1 \_ 0 può autenticare l'utente utilizzando i dati di accesso memorizzati nella cache.

Il \_ pacchetto di autenticazione MSV1 0 supporta anche i [pacchetti](subauthentication-packages.md)di autenticazione. Un pacchetto di sottoautenticazione è una DLL che può sostituire parte dei criteri di autenticazione e di convalida usati dal \_ pacchetto di autenticazione MSV1 0.

Il \_ pacchetto di autenticazione MSV1 0 definisce una coppia chiave/valore stringa di [*credenziali primarie*](../secgloss/p-gly.md) . La stringa di credenziali primarie include le credenziali derivate dai dati forniti al momento dell'accesso. Include il nome utente e i form con distinzione tra maiuscole e minuscole e con distinzione tra maiuscole e minuscole della password dell'utente.

 

 
