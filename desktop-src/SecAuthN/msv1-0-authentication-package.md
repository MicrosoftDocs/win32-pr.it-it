---
description: Microsoft fornisce il pacchetto di autenticazione MSV1 \_ 0 per gli accessi al computer locale che non richiedono l'autenticazione personalizzata.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 Authentication Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12366ecf2ce213b1221fe310e77f9f019c859c038a47d332c8b702639662bc53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921752"
---
# <a name="msv1_0-authentication-package"></a>Pacchetto di autenticazione MSV1 \_ 0

Microsoft fornisce il pacchetto di autenticazione MSV1 \_ 0 per gli accessi al computer locale che non richiedono [](../secgloss/a-gly.md) l'autenticazione personalizzata. [*L'autorità di*](../secgloss/l-gly.md) sicurezza locale (LSA) chiama il pacchetto di autenticazione MSV1 0 per elaborare i dati di accesso raccolti dall'AUTORITÀ DI SICUREZZA per il \_ processo di accesso [*Winlogon.*](../secgloss/w-gly.md) [](../secgloss/g-gly.md) Il pacchetto MSV1 0 controlla il database sam (Security Accounts Manager) locale per determinare se i dati di accesso appartengono a un'entità di sicurezza valida e quindi restituisce il risultato del tentativo di accesso \_ all'account [](../secgloss/s-gly.md) LSA.

MSV1 \_ 0 supporta anche gli accessi al dominio. MSV1 \_ 0 elabora gli accessi al dominio usando l'autenticazione pass-through, come illustrato nel diagramma seguente.

![Pacchetto di autenticazione msv1 \- 0](images/lsaint4.png)

Nell'autenticazione pass-through, l'istanza locale di MSV1 0 usa il servizio Accesso rete per chiamare l'istanza di MSV1 0 in esecuzione nel \_ \_ controller di dominio. L'istanza del controller di dominio di MSV1 0 controlla quindi il database SAM del controller di dominio e restituisce il risultato dell'accesso all'istanza \_ di MSV1 0 nel \_ computer locale. La versione locale di MSV1 0 inoltra il risultato \_ dell'accesso all'istanza di LSA nel computer locale.

Se il controller di dominio non è disponibile [](../secgloss/c-gly.md) e LSA contiene credenziali memorizzate nella cache per l'utente, l'istanza locale di MSV1 0 può autenticare l'utente utilizzando i dati di accesso memorizzati nella \_ cache.

Il pacchetto di autenticazione MSV1 \_ 0 supporta anche i [pacchetti di autenticazione secondaria](subauthentication-packages.md). Un pacchetto di autenticazione secondaria è una DLL che può sostituire parte dei criteri di autenticazione e convalida utilizzati dal pacchetto di autenticazione MSV1 \_ 0.

Il pacchetto di autenticazione MSV1 \_ 0 definisce una [*coppia chiave/valore*](../secgloss/p-gly.md) stringa delle credenziali primaria. La stringa di credenziali primaria contiene le credenziali derivate dai dati forniti al momento dell'accesso. Include il nome utente e i formati con distinzione tra maiuscole e minuscole e senza distinzione tra maiuscole e minuscole della password dell'utente.

 

 
