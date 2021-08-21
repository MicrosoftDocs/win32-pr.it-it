---
description: Alcuni protocolli da cui l'applicazione dipende per determinati servizi, ad esempio RPC (Remote Procedure Call), possono avere strutture e funzioni dipendenti dalla versione IP che richiedono di modificare l'applicazione in termini di utilizzo.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Protocolli sottostanti per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91564f37284927620ba4e8367464c6148229b256d55e70eef756af8c966e2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993231"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a>Protocolli sottostanti per applicazioni Winsock IPv6

Alcuni protocolli da cui l'applicazione dipende per determinati servizi, ad esempio RPC (Remote Procedure Call), possono avere strutture e funzioni dipendenti dalla versione IP che richiedono di modificare l'applicazione in termini di utilizzo.

Parte del processo di modifica del codice per supportare IPv6 deve includere la determinazione se l'uso dei protocolli sottostanti (dal punto di vista dello stack, questi protocolli sono considerati protocolli di livello superiore) richiede la modifica per poter usare correttamente IPv6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida IPv6 per applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture dei dati per le app Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Socket a doppio stack per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> </dl>

 

 



