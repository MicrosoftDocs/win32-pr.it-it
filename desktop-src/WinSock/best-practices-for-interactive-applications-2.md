---
description: Nel morphing del codice di aggiornamento della cella della vita, sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Procedure consigliate per le applicazioni interattive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307047"
---
# <a name="best-practices-for-interactive-applications"></a>Procedure consigliate per le applicazioni interattive

Nel morphing del codice di aggiornamento della cella della vita, sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni. Di seguito sono riportate alcune strategie generali da applicare durante la scrittura di questi tipi di applicazioni:

-   Rendere il flusso di dati quanto più possibile, anziché andare in blocchi.
-   Usare alcune transazioni di grandi dimensioni anziché molte più piccole. Anche le transazioni di grandi dimensioni possono essere trasmesse in modo efficiente.
-   Riconoscere che la rete è una risorsa lenta e non affidabile e sviluppa ogni applicazione per ridurre al minimo la dipendenza sulla rete.
-   Usare una rappresentazione ben progettata dei dati in rete. La rappresentazione dei dati deve essere indipendente dall'architettura del computer, non contenere FAT ed eventualmente essere compressa.
-   Durante l'inizializzazione e l'arresto, non fare in modo che l'utente attenda che la rete venga avviata o arrestata. L'inizializzazione correlata alla rete potrebbe richiedere un tempo relativamente lungo. Separare il codice di rete non critico.
-   Gestire gli errori in base al relativo effetto. Non tutti gli errori sono di importanza critica. Implementare i meccanismi di ripristino e fornire commenti e suggerimenti degli utenti non intrusivi.
-   Utilizzare RPC (Remote Procedure Call) solo quando appropriato. Il protocollo RPC è sincrono in Windows Me/98 e produce sempre un protocollo loquace e FAT quando viene usato per inviare piccole quantità di dati.
-   Misurare l'overhead di rete con netstat; è possibile che si sorprenda la divulgazione delle misurazioni.
-   Testare l'applicazione in un'ampia gamma di reti, in particolare per le reti lente o soggette a perdita. Reti LAN wireless, modem e reti private virtuali (VPN) su Internet sono ottime reti per i test.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



