---
title: Nomi delle entità
description: Per consentire a un client di creare una sessione con autenticazione reciproca con un programma server, deve fornire il nome dell'entità del server previsto.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c0ba17916fb9f9c91ac959ea961c19d0f0a03e31d4caa11784dc123b54c5a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927220"
---
# <a name="principal-names"></a>Nomi delle entità

Per consentire a un client di creare una sessione con autenticazione reciproca con un programma server, deve fornire il nome dell'entità del server previsto. Alcuni protocolli, ad esempio Kerberos, richiedono un nome di entità server corretto per qualsiasi sessione autenticata. Un'entità è un'entità riconosciuta dal sistema di sicurezza. Sono inclusi gli utenti umani e i servizi di sistema. Tutti i nomi delle entità hanno un formato simile per un provider di supporto per la sicurezza (SSP) specificato. Un provider di servizi condivisi è un modulo software che esegue la convalida della sicurezza. Per altre informazioni, vedere [Panoramica dell'architettura SSPI.](sspi-architectural-overview.md) Per mantenere l'uniformità, un provider di sicurezza assegna in genere ai servizi di sistema nomi simili a quelli degli utenti. In alcuni provider di sicurezza, i servizi di sistema potrebbero non avere un nome di entità.

Il server registra il nome dell'entità per il provider di sicurezza usando la [**funzione RpcServerRegisterAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Per ogni provider di sicurezza è possibile usare un solo nome di entità server. Se vengono registrati più nomi, viene scelto e usato in modo casuale un nome. Il provider di servizi condivisi determina il formato del nome dell'entità. Ad esempio, gli SSP Kerberos/Negotiate per un servizio di sistema hanno un aspetto simile al seguente: nome \_ computer$ @childdomain.parentdomain1.parentdomain2.COM .

La procedura consigliata per la generazione di nomi di entità è l'uso di API documentate (ad esempio la funzione **DsMakeSpn),** anziché eseguire il piecing del nome dell'entità dalle stringhe. L'uso di API documentate aumenta la portabilità tra ambienti di distribuzione diversi ed elimina la possibilità di errori.

Se si specifica un nome di entità non corretto, il client e il server potrebbero non stabilire una sessione autenticata. Il provider di servizi condivisi SCHANNEL accetta i nomi delle entità in uno dei due formati seguenti:

-   Il primo formato del nome dell'entità SCHANNEL è [*il formato msstd.*](m-glos.md) I nomi in formato msstd in genere seguono il modello msstd:servername@serverdomain.com . Questa proprietà viene definita proprietà del nome di posta elettronica. Se il certificato contiene una proprietà del nome di posta elettronica e contiene il simbolo chiocciola (@), il nome dell'entità è msstd:email name. In caso contrario, deve contenere la proprietà del nome comune. Le barre rovesciate interne vengono raddoppiate, proprio come nelle associazioni di stringhe.
-   Il secondo formato del nome dell'entità SCHANNEL è [*il formato completo.*](f-glos.md) Si tratta di una serie di nomi conformi a RFC1779 delimitati da parentesi angolari e separati da barre rovesciate. In genere segue il modello fullsic: \\ < \\ Authority \\ SubAuthority \\ ..... \\ Person> or fullsic: \\ < \\ Authority \\ SubAuthority \\ ..... \\ ServerProgram>.

Se il nome non corrisponde al certificato, viene restituito ERROR \_ ACCESS \_ DENIED. Se il formato del nome non è valido, SSP SCHANNEL restituisce il codice ERROR \_ INVALID \_ PARAMETER.

Per eseguire una query sul nome dell'entità del server, le applicazioni possono chiamare [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). In questo modo viene allocata una stringa con terminazione Null per contenere il nome dell'entità. Prima che termini, l'applicazione deve richiamare [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per rilasciare la memoria occupata da questa stringa.

L'esecuzione di query sul nome del server in questo modo non è sicura e deve essere evitata. Per l'autenticazione server, il programma client deve conoscere il server a cui si connette e deve creare il nome dell'entità server da zero.

 

 




