---
description: La longevità di IPv4 ha comportato la codifica hardware di molti indirizzi IPv4 noti, ad esempio gli indirizzi di loopback (127. x. x. x), le costanti integer come il loopback inaddr \_ , tra gli altri.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Utilizzo di indirizzi IPv4 hardcoded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343456"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Utilizzo di indirizzi IPv4 hardcoded

La longevità di IPv4 ha comportato la codifica hardware di molti indirizzi IPv4 noti, ad esempio gli indirizzi di loopback (127. x. x. x), le costanti integer come il loopback inaddr \_ , tra gli altri. La pratica della codifica hardware di questi indirizzi presenta problemi evidenti quando si modifica un'applicazione esistente per il supporto di IPv6 o la creazione di nuovi programmi indipendenti dalla versione.

Procedura consigliata

-   L'approccio migliore consiste nell'evitare il hardcoded degli indirizzi.

Codice da evitare

-   Evitare di utilizzare indirizzi hardcoded nel codice.

**Per modificare la codebase esistente da IPv4 a IPv4 e IPv6-interoperabilità**

1.  Acquisire l'utilità *Checkv4.exe* . L'utilità *Checkv4.exe* viene installata come parte di Microsoft Windows Software Development Kit (SDK) rilasciata per Windows Vista e versioni successive. Il Windows SDK è disponibile tramite un abbonamento MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) .
2.  Eseguire l'utilità *Checkv4.exe* sul codice. Per informazioni su come eseguire l'utilità di *Checkv4.exe* sui file, vedere la sezione relativa all' [uso dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  L'utilità *Checkv4.exe* segnala la presenza di definizioni comuni per gli indirizzi IPv4, ad esempio il loopback inaddr \_ . Modificare il codice che utilizza stringhe letterali con codice indipendente dalla versione del protocollo.
4.  Eseguire una ricerca nella codebase per altre stringhe letterali potenziali, a seconda dei casi.

L'utilità *Checkv4.exe* può essere utile per trovare stringhe letterali comuni, ma potrebbero essere presenti altre specifiche per l'applicazione. È consigliabile eseguire ricerche e test completi per assicurarsi che la codebase abbia eliminato i potenziali problemi associati alle stringhe letterali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture di dati per applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Socket dual stack per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Problemi dell'interfaccia utente per le applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



