---
description: La longevità di IPv4 ha comportato la codifica hard-coding di molti indirizzi IPv4 noti, ad esempio indirizzi di loopback (127.x.x.x), costanti integer come INADDR LOOPBACK, tra gli \_ altri.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso di indirizzi IPv4 hardcoded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0506f200776402464c4b2904435157c435ece7fc2c6d9e0b10bfd1c1d66491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121201"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Uso di indirizzi IPv4 hardcoded

La longevità di IPv4 ha comportato la codifica hard-coding di molti indirizzi IPv4 noti, ad esempio indirizzi di loopback (127.x.x.x), costanti integer come INADDR LOOPBACK, tra gli \_ altri. La procedura di hard coding di questi indirizzi presenta problemi evidenti quando si modifica un'applicazione esistente per supportare IPv6 o si creano nuovi programmi indipendenti dalla versione IP.

Procedura consigliata

-   L'approccio migliore consiste nell'evitare la hardcoding di qualsiasi indirizzo.

Codice da evitare

-   Evitare di usare indirizzi hardcoded nel codice.

**Per modificare la codebase esistente da IPv4 a IPv4 e IPv6-interoperability**

1.  Acquisire *l'Checkv4.exe* di configurazione. *LCheckv4.exe* utility viene installata come parte di Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive. L Windows SDK è disponibile tramite una sottoscrizione MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) .
2.  Eseguire *l'utilitàCheckv4.exe* sul codice. Informazioni su come eseguire *l'utilitàCheckv4.exe* sui file nella sezione uso dell'utilità [Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  *LCheckv4.exe'utilità* segnala la presenza di definisce comuni per gli indirizzi IPv4, ad esempio INADDR \_ LOOPBACK. Modificare qualsiasi codice che usa stringhe letterali con codice indipendente dalla versione del protocollo.
4.  Cercare nella codebase altre potenziali stringhe letterali, in base alle esigenze.

*LCheckv4.exe* utilità può essere utile per trovare stringhe letterali comuni, ma potrebbero essere presenti altre specifiche per l'applicazione. È consigliabile eseguire ricerche e test approfonditi per assicurarsi che la codebase abbia cancellato potenziali problemi associati alle stringhe letterali.

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

[Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



