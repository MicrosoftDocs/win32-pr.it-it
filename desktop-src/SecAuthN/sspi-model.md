---
description: Security Support Provider Interface (SSPI) consente a un'applicazione di usare vari modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia nel sistema di sicurezza.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modello SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5d915a8937f57105e2478b41955cc5789fba25791e7f118a84dc4fa38e12fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916818"
---
# <a name="sspi-model"></a>Modello SSPI

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) consente a un'applicazione di usare vari modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia nel sistema di sicurezza. SSPI non stabilisce le credenziali [*di accesso*](../secgloss/c-gly.md) perché si tratta in genere di un'operazione con privilegi gestita dal sistema operativo.

Un [*provider di supporto per*](../secgloss/s-gly.md) la sicurezza (SSP) è contenuto in una libreria [](../secgloss/s-gly.md) a collegamento dinamico (DLL) che implementa SSPI rendendo disponibili uno o più pacchetti di sicurezza per le applicazioni. [](../secgloss/d-gly.md) Ogni pacchetto di sicurezza fornisce mapping tra le chiamate di funzione SSPI di un'applicazione e le funzioni di un modello di sicurezza effettivo. I pacchetti di sicurezza [*supportano protocolli di*](../secgloss/s-gly.md) sicurezza come [*l'autenticazione Kerberos*](../secgloss/k-gly.md) e LAN Manager.

L'interfaccia SSPI è disponibile sia in modalità kernel che in modalità utente. Per usare la funzionalità SSPI in modalità kernel, è necessario installare la Windows DDK del file system installabile. Il modello chiamante rimane invariato, ma le considerazioni sulla modalità kernel vengono riportate nelle pagine di riferimento delle funzioni. Per altre informazioni, vedere [Funzioni SSPI](authentication-functions.md).

 

 
