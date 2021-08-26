---
description: Nel morphing del codice di aggiornamento delle celle Life sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Procedure consigliate per le applicazioni interattive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497fc56419f8859b7490671590b4589092c4c5b37047a01b0bf80cee9bf8c213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996901"
---
# <a name="best-practices-for-interactive-applications"></a>Procedure consigliate per le applicazioni interattive

Nel morphing del codice di aggiornamento delle celle Life sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni. Alcune strategie generali da applicare quando si scrivono questi tipi di applicazioni sono:

-   Rendere il flusso di dati il più possibile, anziché essere in blocchi.
-   Usare alcune transazioni di grandi dimensioni anziché molte transazioni di piccole dimensioni. Anche le transazioni di grandi dimensioni possono essere trasmesse in modo efficiente.
-   Riconoscere che la rete è una risorsa lenta e inaffidabile e sviluppare ogni applicazione per ridurre al minimo la propria affidabilità nella rete.
-   Usare una rappresentazione ben progettata dei dati nella rete. La rappresentazione dei dati deve essere indipendente dall'architettura del computer, non contenere alcun contenuto ed eventualmente essere compressa.
-   Durante l'inizializzazione e l'arresto, non fare in modo che l'utente attenda l'avvio o l'arresto della rete. L'inizializzazione correlata alla rete potrebbe richiedere un tempo relativamente lungo. Separare il codice di rete non critico.
-   Gestire gli errori in base all'impatto. Non tutti gli errori sono critici. Implementare meccanismi di ripristino e fornire feedback utente non intrusivo.
-   Usare le chiamate di procedura remota (RPC) solo quando appropriato. RPC è sincrono in Windows Me/98 e comporta sempre protocolli poco comuni quando vengono usati per inviare piccole quantità di dati.
-   Misurare il sovraccarico della rete usando Netstat; ci si può sorprendere di ciò che rivelano le misurazioni.
-   Testare l'applicazione in un'ampia gamma di reti, in particolare reti lente o erre. Le reti LAN wireless, i modem e le reti private virtuali (VPN) su Internet sono reti buone per i test.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni socket Windows ad alte prestazioni](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



