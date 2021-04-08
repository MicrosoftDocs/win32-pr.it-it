---
title: Come un servizio compone i relativi nomi SPN
description: Un servizio può utilizzare due funzioni per comporre i relativi SPN DsGetSpn è una funzione generica per la composizione di SPN e DsServerRegisterSpn è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome dell'entità servizio AD, come compone un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855429"
---
# <a name="how-a-service-composes-its-spns"></a>Come un servizio compone i relativi nomi SPN

Un servizio può utilizzare due funzioni per comporre i relativi nomi SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) è una funzione generica per la composizione di SPN e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.

Un programma di installazione del servizio usa in genere la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre i nomi SPN, che vengono quindi registrati nell'account di accesso del servizio usando la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) . **DsGetSpn** può eseguire le funzioni seguenti.

-   Creare un nome SPN semplice con il <service class> / <host> formato "" per un servizio basato su host.
-   Creare un nome SPN complesso che includa il &lt; componente "nome servizio &gt; " utilizzato dai servizi replicabili o il &lt; componente "porta &gt; " che distingue più istanze di un servizio in un singolo host.
-   Per impostazione predefinita, creare un singolo SPN con il &lt; componente "host &gt; " impostato sul nome di un host specificato o sul nome del computer locale.
-   Creare una matrice di nomi SPN per più istanze del servizio che vengono eseguite su più host in tutta la foresta. Ogni SPN specifica il nome dell'host per un'istanza del servizio.
-   Creare una matrice di nomi SPN per più istanze del servizio che vengono eseguite nello stesso host. Ogni SPN specifica il nome dell'host e un numero di porta per un'istanza del servizio.

La matrice di nomi restituiti da [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve essere liberata chiamando la funzione [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .

Tenere presente che le funzioni [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) non verificano che i nomi SPN siano univoci. Poiché l'autenticazione reciproca non riesce se un client presenta un nome SPN non univoco, verificare l'univocità prima di registrare un nome SPN. A tale scopo, eseguire una ricerca nel catalogo globale (GC) per gli attributi **servicePrincipalName** che corrispondono al nome SPN. Per ulteriori informazioni sulla ricerca nel GC, vedere la pagina relativa alla [ricerca nel catalogo globale](searching-global-catalog-contents.md).

 

 




