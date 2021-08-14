---
title: Modalità di composizione dei nomi SPN da parte di un servizio
description: Un servizio può usare due funzioni per comporre i nomi SPN DsGetSpn è una funzione di utilizzo generico per la composizione di nomi SPN e DsServerRegisterSpn è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome dell'entità servizio AD, modalità di composizione di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd4c0ac9c871c76e9e8771a688d203898674e477426ebd788ee34fe894011a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188645"
---
# <a name="how-a-service-composes-its-spns"></a>Modalità di composizione dei nomi SPN da parte di un servizio

Un servizio può usare due funzioni per comporre i nomi SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) è una funzione di utilizzo generico per la composizione di nomi SPN e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.

Un programma di installazione del servizio usa in genere la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre nomi SPN, che viene quindi registrato nell'account di accesso del servizio usando [**la funzione DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) **DsGetSpn può** eseguire le funzioni seguenti.

-   Creare un nome SPN semplice con il <service class> / <host> formato " " per un servizio basato su host.
-   Creare un nome SPN complesso che includa il componente " service name " usato dai servizi replicabili o dal componente " port " che distingue più istanze di un servizio &lt; &gt; in un singolo &lt; &gt; host.
-   Creare un singolo nome SPN con il componente " host " impostato sul nome di un host specificato o sul nome &lt; del computer locale per impostazione &gt; predefinita.
-   Creare una matrice di nomi SPN per più istanze del servizio che verranno eseguite in più host in tutta la foresta. Ogni nome SPN specifica il nome dell'host per un'istanza del servizio.
-   Creare una matrice di nomi SPN per più istanze del servizio che verranno eseguite nello stesso host. Ogni nome SPN specifica il nome dell'host e un numero di porta per un'istanza del servizio.

La matrice di nomi restituita [**da DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve essere liberata chiamando la [**funzione DsFreeSpnArray.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)

Tenere presente che le funzioni [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) non verificano che i nomi SPN siano univoci. Poiché l'autenticazione reciproca ha esito negativo se un client presenta un nome SPN non univoco, verificare l'univocità prima di registrare un nome SPN. A tale scopo, cercare nel catalogo globale (GC) gli **attributi servicePrincipalName** che corrispondono al nome SPN. Per altre informazioni sulla ricerca nel catalogo globale, vedere [Ricerca nel catalogo globale](searching-global-catalog-contents.md).

 

 




