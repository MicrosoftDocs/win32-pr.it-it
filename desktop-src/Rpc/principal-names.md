---
title: Nomi principali
description: Affinché un client crei una sessione con autenticazione reciproca con un programma server, deve fornire il nome principale previsto del server.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471651"
---
# <a name="principal-names"></a>Nomi principali

Affinché un client crei una sessione con autenticazione reciproca con un programma server, deve fornire il nome principale previsto del server. Alcuni protocolli, ad esempio Kerberos, richiedono un nome dell'entità server corretto per qualsiasi sessione autenticata. Un'entità è un'entità riconosciuta dal sistema di sicurezza. Sono inclusi gli utenti umani e i servizi di sistema. Tutti i nomi di entità hanno un formato simile per un determinato Security Support Provider (SSP). Un SSP è un modulo software che esegue la convalida della sicurezza. Per ulteriori informazioni, vedere [Cenni preliminari sull'architettura di SSPI](sspi-architectural-overview.md). Per mantenere uniformità, un provider di sicurezza in genere fornisce ai servizi di sistema nomi simili come gli utenti. In alcuni provider di sicurezza, i servizi di sistema potrebbero non avere un nome di entità.

Il server registra il nome principale per il provider di sicurezza utilizzando la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Per ogni provider di sicurezza è possibile utilizzare un solo nome entità server. Se è registrato più di un nome, un nome viene scelto in modo casuale e viene usato. Il provider di servizi condivisi determina il formato del nome dell'entità. Ad esempio, i SSP Kerberos/Negotiate per un servizio di sistema hanno un aspetto simile al seguente: \_ nome computer $ @childdomain.parentdomain1.parentdomain2.COM .

La procedura consigliata per la generazione di nomi principali consiste nell'usare API documentate, ad esempio la funzione **DsMakeSpn** , anziché riunire il nome principale dalle stringhe. L'uso di API documentate consente di aumentare la portabilità tra diversi ambienti di distribuzione ed elimina la possibilità di errori.

La specifica di un nome di entità non corretto potrebbe impedire al client e al server di stabilire una sessione autenticata. SSP SCHANNEL accetta nomi principali in uno dei due formati seguenti:

-   Il primo form del nome principale SCHANNEL è il modulo [*msstd*](m-glos.md) . I nomi nel form msstd in genere seguono il modello msstd:servername@serverdomain.com . Questa proprietà viene definita nome di posta elettronica. Se il certificato contiene una proprietà del nome di posta elettronica e contiene il simbolo di chiocciola (@), il nome dell'entità è msstd: email name. In caso contrario, deve contenere la proprietà nome comune. Le barre rovesciate interne sono doppie, come nelle associazioni di stringa.
-   Il secondo formato del nome principale SCHANNEL è il modulo [*fullsic*](f-glos.md) . Si tratta di una serie di nomi conformi a RFC1779 delimitati da parentesi angolari e separati da barre rovesciate. In genere segue il modello fullsic: \\ < \\ Authority \\ subauthorization \\ .... \\ . Persona> o fullsic: \\ < \\ \\ sottoautorizzazione autorità \\ .... \\> ServerProgram.

Se il nome non corrisponde al certificato, viene restituito l'errore di \_ accesso \_ negato. Se il formato del nome non è valido, SCHANNEL SSP restituisce il parametro ERROR del codice \_ non valido \_ .

Per eseguire una query per il nome dell'entità del server, le applicazioni possono chiamare [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). In questo modo viene allocata una stringa con terminazione null in cui è contenuto il nome dell'entità. Prima di terminare, l'applicazione deve richiamare [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per rilasciare la memoria occupata da questa stringa.

L'esecuzione di query per il nome del server in questo modo non è sicura e deve essere evitata. Per l'autenticazione server, il programma client deve essere in grado di individuare il server a cui si connette e deve creare il nome dell'entità server da zero.

 

 




