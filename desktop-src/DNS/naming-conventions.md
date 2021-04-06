---
title: Convenzioni di denominazione
description: Le convenzioni di denominazione condividono un obiettivo comune per risolvere in modo non ambiguo un nome in un indirizzo di rete, in genere un indirizzo IP. La differenza tra le convenzioni di denominazione è l'approccio distinto di ogni convenzione alla risoluzione dei nomi.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044999"
---
# <a name="naming-conventions"></a>Convenzioni di denominazione

Le convenzioni di denominazione condividono un obiettivo comune: per risolvere in modo non ambiguo un nome in un indirizzo di rete, in genere un indirizzo IP. La differenza tra le convenzioni di denominazione è l'approccio distinto di ogni convenzione alla risoluzione dei nomi.

Per identificare i computer in diversi metodi di risoluzione dei nomi di sistema, incluso il metodo Windows 2000, vengono usate le convenzioni di denominazione seguenti:

-   [Nome computer](#computer-name)
-   [Nome host](#host-name)
-   [Nome di dominio completo (FQDN)](#fully-qualified-domain-name)
-   [Nome distinto relativo](#relative-distinguished-name)

## <a name="computer-name"></a>Nome computer

Nello spazio dei nomi NetBIOS Flat, un singolo nome risolve in modo non ambiguo un nome di computer in un indirizzo di rete. Questo è il nome che le versioni precedenti di Windows sono state archiviate in browser e nel browser master, abilitando le reti peer Windows per l'esplorazione delle risorse nei computer Windows in rete. In questo scenario, il termine associato al computer era il *nome del computer*. La registrazione del nome del computer dipende dalle trasmissioni di rete (e da un browser master, determinato dalle elezioni vinte da numeri di versione di Windows successivi o da un utilizzo di Windows NT o da una combinazione). Si tratta di un'operazione utile per le piccole reti di Windows basate su peer, ma le reti si sono rivelate presto più diffuse.

## <a name="host-name"></a>Nome host

A questo punto è arrivato il Naming Service Windows Internet (WINS), che ha abilitato un repository dinamico e centralizzato di nomi di computer basati su NetBIOS archiviati nei server WINS. Questi repository possono servire una rete di dimensioni maggiori. Con questo sviluppo, le query di risoluzione dei nomi potrebbero essere indirizzate a un server WINS (anziché trasmettere) e i conflitti potrebbero essere Arbitrated a livello centrale. Con WINS, il termine nome computer è stato mantenuto, ma il termine *nome host* è comparso ed è stato usato in modo intercambiabile con il nome del computer. Al momento, WINS era il sistema di risoluzione dei nomi predefinito per le piattaforme Windows, ma il DNS stava ottenendo la popolarità e la proliferazione di reti più grandi e più grandi.

Le reti aumentano e WINS diventa meno in grado di gestire il volume di nomi crescente. La riduzione della capacità di WINS per gestire il carico per la risoluzione dei nomi non era dovuta alla potenza di elaborazione necessaria per la risoluzione, ma al fatto che la generazione di nomi univoci per molti computer diventava un carico di gestione sempre maggiore.

## <a name="fully-qualified-domain-name"></a>Nome di dominio completo

DNS è una soluzione migliore. con lo spazio dei nomi gerarchico, la necessità di nomi di computer univoci è isolata in un determinato dominio, consentendo a un nome di computer, ad esempio *Server1* , di esistere in posizioni di dominio diverse nella stessa gerarchia. Con la possibilità di avere lo stesso nome host in domini diversi, la necessità è nata per un nome che ha risolto correttamente la gerarchia DNS. Il nome deve includere non solo il nome del computer o il nome host, ma anche un nome che può identificare in modo univoco o qualificare completamente tale computer all'interno dell'intera gerarchia DNS. Tale nome è il [*nome di dominio*](f-gly.md) completo (FQDN), ad esempio Server1.widgets.Microsoft.com.

In alcune situazioni, tuttavia, la parte della gerarchia del dominio FQDN è complessa e un nome locale per un determinato computer (o qualsiasi altro host DNS) relativo al dominio DNS in cui risiede l'host è necessario. Tale nome è il [*nome distinto relativo*](r-gly.md). Il nome distinto relativo è semplicemente il nome host singolo a sinistra del punto più a sinistra nel nome di dominio completo, in modo che un FQDN di server1.widgets.microsoft.com includa Server1 come nome distinto relativo.

## <a name="relative-distinguished-name"></a>Nome distinto relativo

Anziché imporre nuovi nomi o nuove convenzioni di denominazione per gli utenti di nomi NetBIOS, DNS usa semplicemente il nome del computer (nome host) come nome distinto relativo e aggiunge la gerarchia di dominio DNS a tale nome per creare il nome di dominio completo. Nella figura seguente viene illustrato come identificare la parte relativa al nome del computer (o nome host o nome distinto relativo) dell'FQDN:

![associazione tra RDN e gerarchia di domini DNS per creare un FQDN](images/fqdn.png)

 

 




