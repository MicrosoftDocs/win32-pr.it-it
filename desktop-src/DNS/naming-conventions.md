---
title: Convenzioni di denominazione
description: Le convenzioni di denominazione condividono un obiettivo comune di risolvere senza ambiguità un nome in un indirizzo di rete, in genere un indirizzo IP. La differenza tra le convenzioni di denominazione risiede nell'approccio distinto di ogni convenzione alla risoluzione dei nomi.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b378f9383f773cb24fb47c81cb92a066094a4ce528d7f3710212c6bb7cac0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076590"
---
# <a name="naming-conventions"></a>Convenzioni di denominazione

Le convenzioni di denominazione condividono un obiettivo comune: risolvere senza ambiguità un nome in un indirizzo di rete, in genere un indirizzo IP. La differenza tra le convenzioni di denominazione risiede nell'approccio distinto di ogni convenzione alla risoluzione dei nomi.

Le convenzioni di denominazione seguenti vengono usate per identificare i computer in vari metodi di risoluzione dei nomi di sistema, incluso Windows 2000:

-   [Nome computer](#computer-name)
-   [Nome host](#host-name)
-   [Nome di dominio completo (FQDN)](#fully-qualified-domain-name)
-   [Nome distinto relativo](#relative-distinguished-name)

## <a name="computer-name"></a>Nome computer

Nello spazio dei nomi NetBIOS flat, un singolo nome risolve senza ambiguità il nome di un computer in un indirizzo di rete. Si tratta del nome che le versioni precedenti Windows archiviate negli elenchi del browser e del browser master, consentendo alle reti peer Windows di esplorare le risorse nei computer Windows rete. In questo scenario, il termine associato al computer era nome *computer*. La registrazione del nome del computer dipendeva dalle trasmissioni di rete (e da un browser master, determinato dal numero di versione Windows o dall'utilizzo di Windows NT o da una combinazione successiva). Ciò è stato utile per reti di Windows di piccole dimensioni basate su peer, ma le reti sono aumentate ben presto oltre ciò che l'uso di trasmissioni e semplici elenchi di browser master per file flat potrebbe essere utile.

## <a name="host-name"></a>Nome host

Successivamente è stato Windows internet Naming Service (WINS), che ha abilitato un repository dinamico e centralizzato di nomi di computer basati su NetBIOS archiviati nei server WINS. Questi repository potrebbero essere in grado di eseguire operazioni su una rete più grande. Con questo sviluppo, le query di risoluzione dei nomi potrebbero essere indirizzate a un server WINS (anziché essere trasmesse) e i conflitti potrebbero essere arbitrati centralmente. Con WINS, il termine nome computer è stato mantenuto, ma anche il termine *nome host* è stato visualizzato e è stato utilizzato in modo intercambiabile con il nome del computer. A quel tempo, WINS era il sistema di risoluzione dei nomi predefinito per le piattaforme Windows, ma DNS stava acquisiscendo la popolarità e la proliferazione di reti di grandi e grandi dimensioni.

Le reti sono aumentate e WINS è diventato meno in grado di gestire il volume crescente di nomi. La capacità decrescente di WINS di gestire il carico di risoluzione dei nomi non è dovuta alla potenza di elaborazione necessaria per la risoluzione, ma al fatto che la generazione di nomi univoci per molti computer è diventata un carico di gestione in continua crescita.

## <a name="fully-qualified-domain-name"></a>Nome di dominio completo

DNS è una soluzione migliore. con lo spazio dei nomi gerarchico, la necessità di nomi di computer univoci è isolata in un determinato dominio, consentendo a un nome computer, ad esempio *server1,* di esistere in percorsi di dominio diversi nella stessa gerarchia. Con la possibilità di avere lo stesso nome host in domini diversi, è necessario un nome che indirizza correttamente la gerarchia DNS. Il nome deve includere non solo il nome del computer o il nome host, ma anche un nome che potrebbe identificare in modo univoco, o qualificare completamente, il computer all'interno dell'intera gerarchia DNS. Tale nome è [*il nome di dominio completo*](f-gly.md) (FQDN), ad esempio server1.widgets.microsoft.com.

Tuttavia, in determinate situazioni, la parte della gerarchia di dominio del nome di dominio completo è complicata e è necessario un nome locale per un determinato computer (o qualsiasi altro host DNS) relativo al dominio DNS in cui risiede l'host. Tale nome è il [*nome distinto relativo*](r-gly.md). Il nome distinto relativo è semplicemente il nome host singolo a sinistra del punto più a sinistra nel nome di dominio completo, in modo che un nome fqdn di server1.widgets.microsoft.com abbia server1 come nome distinto relativo.

## <a name="relative-distinguished-name"></a>Nome distinto relativo

Invece di imporre nuovi nomi o nuove convenzioni di denominazione agli utenti di nomi NetBIOS, DNS usa semplicemente il nome computer (nome host) come nome distinto relativo e aggiunge la gerarchia di domini DNS a tale nome per creare il nome FQDN. La figura seguente illustra come identificare la parte del nome computer (o del nome host o del nome distinto relativo) dell'FQDN:

![Rdn e dns domain hierarchy combine to create a fqdn (Combinazione della gerarchia di domini rdn e DNS per creare un nome di dominio completo)](images/fqdn.png)

 

 




