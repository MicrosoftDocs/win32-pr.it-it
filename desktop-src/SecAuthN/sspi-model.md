---
description: Security Support Provider Interface (SSPI) consente a un'applicazione di usare diversi modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia del sistema di sicurezza.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modello SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401575"
---
# <a name="sspi-model"></a>Modello SSPI

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) consente a un'applicazione di usare diversi modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia del sistema di sicurezza. SSPI non stabilisce [*credenziali*](../secgloss/c-gly.md) di accesso perché si tratta in genere di un'operazione con privilegi gestita dal sistema operativo.

Una [*Security Support Provider*](../secgloss/s-gly.md) (SSP) è contenuta in una [*libreria di collegamento dinamico*](../secgloss/d-gly.md) (dll) che implementa SSPI rendendo disponibili per le applicazioni uno o più [*pacchetti di sicurezza*](../secgloss/s-gly.md) . Ogni pacchetto di sicurezza fornisce mapping tra le chiamate di funzione SSPI di un'applicazione e le funzioni di un modello di sicurezza effettivo. I pacchetti di sicurezza supportano i [*protocolli di sicurezza*](../secgloss/s-gly.md) , ad esempio l'autenticazione [*Kerberos*](../secgloss/k-gly.md) e la gestione LAN.

L'interfaccia SSPI è disponibile in modalità kernel e in modalità utente. Per utilizzare la funzionalità SSPI in modalità kernel, è necessario installare il file System di Windows installabile con estensione DDK. Il modello chiamante rimane invariato, ma le considerazioni sulla modalità kernel sono indicate nelle pagine di riferimento per le funzioni. Per ulteriori informazioni, vedere [funzioni SSPI](authentication-functions.md).

 

 
