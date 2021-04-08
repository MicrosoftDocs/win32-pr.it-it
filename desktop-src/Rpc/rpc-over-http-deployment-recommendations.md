---
title: Raccomandazioni sulla distribuzione RPC su HTTP
description: In questa sezione vengono documentate le procedure consigliate e le configurazioni di distribuzione consigliate per ottenere la massima sicurezza e prestazioni quando si utilizza RPC su HTTP.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8871686d1fc8b87bcd6fb7ac4314b1977252f23a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045171"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Raccomandazioni sulla distribuzione RPC su HTTP

In questa sezione vengono documentate le procedure consigliate e le configurazioni di distribuzione consigliate per ottenere la massima sicurezza e prestazioni quando si utilizza RPC su HTTP. Le varie configurazioni trovate in questo documento si applicano a organizzazioni diverse in base a vari requisiti di dimensioni, budget e sicurezza. Ogni configurazione fornisce anche considerazioni sulla distribuzione utili per determinare quale sia la soluzione migliore per uno scenario specifico.

Per informazioni sugli scenari RPC con volume elevato su HTTP, vedere [Microsoft RPC Load Balancing](rpc-load-balancing.md).

Le indicazioni seguenti si applicano a tutte le configurazioni:

-   Usare le versioni di Windows che supportano RPC su HTTP V2.
-   Inserire IIS nel computer che esegue il proxy RPC in modalità IIS 6,0.
-   Non consentire l'accesso anonimo alla directory virtuale del proxy RPC.
-   Non abilitare mai la chiave del registro di sistema AllowAnonymous.
-   Fare in modo che i client RPC over HTTP usino **CertificateSubjectField** (vedere [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per altre informazioni) per verificare che il proxy RPC a cui si è connessi sia il proxy RPC che si prevede.
-   Configurare la chiave del registro di sistema **ValidPorts** in modo che contenga solo i computer a cui si connetteranno i client RPC su http.
-   Non usare caratteri jolly nella chiave **ValidPorts** . Questa operazione consente di risparmiare tempo, ma un computer completamente imprevisto può adattarsi anche al carattere jolly.
-   Usare SSL su client RPC su HTTP. Se vengono seguite le linee guida stabilite in queste sezioni, il client RPC su HTTP non sarà in grado di connettersi senza usare SSL.
-   Configurare RPC su client HTTP per utilizzare la crittografia RPC oltre a usare SSL. Se il client RPC su HTTP non è in grado di raggiungere il KDC, può utilizzare solo Negotiate e NTLM.
-   Configurare i computer client per l'uso di NTLMv2. Impostare la chiave del registro di sistema **LMCompatibilityLevel** su 2 o una versione successiva. Per ulteriori informazioni sulla chiave **LMCompatibilityLevel** , vedere **MSDN.Microsoft.com** .
-   Eseguire una Web farm di computer proxy RPC con la configurazione illustrata in precedenza.
-   Distribuire un firewall tra Internet e il proxy RPC.
-   Per ottenere prestazioni ottimali, configurare IIS in modo da inviare una breve risposta ai codici di errore non riusciti. Poiché il consumer della risposta IIS è un processo automatizzato, non sono necessarie spiegazioni semplici da inviare al client; verranno semplicemente ignorati dal client RPC su HTTP.

Gli obiettivi di base del proxy RPC dal punto di vista della sicurezza, delle prestazioni e della gestibilità sono i seguenti:

-   Fornire un singolo punto di ingresso per il traffico RPC su HTTP nella rete del server. La presenza di un singolo punto di ingresso per il traffico RPC su HTTP in una rete server presenta due vantaggi principali. Innanzitutto, poiché il proxy RPC si trova in Internet, la maggior parte delle organizzazioni isola tali computer in una rete speciale denominata rete perimetrale non attendibile che è separata dalla normale rete aziendale. I server in una rete perimetrale non attendibile vengono gestiti, configurati e monitorati in modo molto accurato per poter resistere ad attacchi provenienti da Internet. Il minor numero di computer in una rete perimetrale non attendibile, più semplice è la configurazione, la gestione, il monitoraggio e la protezione. In secondo luogo, poiché una singola Web farm con proxy RPC installati può servire un numero qualsiasi di server RPC su HTTP che risiedono nella rete aziendale, è molto utile separare il proxy RPC dal server RPC su HTTP e fare in modo che il proxy RPC risieda in una rete perimetrale non attendibile. Se il proxy RPC si trovava nello stesso computer del server RPC su HTTP, le organizzazioni verrebbero forzate a inserire tutti i server back-end in una rete perimetrale non attendibile, il che renderebbe molto più difficile tenere protetta la rete perimetrale non attendibile. La separazione del ruolo del proxy RPC e del server RPC su HTTP consente alle organizzazioni di tenere il numero di computer in una rete perimetrale non attendibile gestibile e quindi più sicuro.
-   Fungere da fusibile di sicurezza per la rete del server. Il proxy RPC è progettato come un fusibile utilizzabile per la rete del server. Se si verifica un errore nel proxy RPC, è sufficiente che protegga il server RPC reale su HTTP. Se le procedure consigliate descritte in questa sezione sono state seguite finora, il traffico RPC su HTTP viene crittografato con la crittografia RPC, oltre a SSL. La crittografia RPC stessa è tra il client e il server, non tra il client e il proxy. Ciò significa che il proxy non riconosce e non è in grado di decrittografare il traffico RPC ricevuto. Riconosce solo alcune sequenze di controllo inviate dal client che gestiscono lo stabilimento di connessione, il controllo di flusso e altri dettagli di tunneling. Non ha accesso ai dati inviati dal client RPC su HTTP al server. Inoltre, il client RPC su HTTP deve autenticarsi in modo indipendente sia per il proxy RPC che per il server RPC su HTTP. In questo modo viene fornita una difesa approfondita. Se il computer proxy RPC viene compromesso, a causa di un errore di configurazione o di una violazione della sicurezza di qualche tipo, i dati che passano attraverso di essi sono ancora protetti da manomissioni. Un utente malintenzionato che ottiene il controllo del proxy RPC può interrompere il traffico, ma non leggerlo o manometterlo. Si tratta del punto in cui entra in gioco il ruolo fuse del proxy RPC, che è spendibile senza che venga compromessa la sicurezza del traffico RPC su HTTP.
-   Distribuire alcune operazioni di controllo e decrittografia degli accessi tra più computer che eseguono proxy RPC in una Web farm. Funzionando correttamente in una Web farm, il proxy RPC consente alle organizzazioni di eseguire l'offload della decrittografia SSL e di alcuni controlli di accesso, liberando così una maggiore capacità sul server back-end per l'elaborazione. L'utilizzo di una Web farm di computer proxy RPC consente inoltre a un'organizzazione di aumentare la propria capacità di resistere agli attacchi Denial of Service (DoS) aumentando la capacità dei server front-end.

All'interno delle linee guida stabilite finora, le organizzazioni hanno ancora scelte. Ogni organizzazione ha scelte e compromessi tra gli inconvenienti degli utenti, la sicurezza e i costi:

-   **Utilizzare l'autenticazione di base o l'autenticazione integrata di Windows per eseguire l'autenticazione al proxy RPC?** RPC su HTTP supporta attualmente solo NTLM, non supporta Kerberos. Inoltre, se è presente un proxy HTTP o un firewall tra il client RPC su HTTP e il proxy RPC che inserisce il pragma *via* nell'intestazione HTTP, l'autenticazione NTLM non funzionerà. In caso contrario, le organizzazioni possono scegliere tra l'autenticazione di base e NTLM. Il vantaggio dell'autenticazione di base è che è più veloce e più semplice e pertanto offre meno opportunità di attacchi Denial of Service. Ma NTLM è più sicuro. A seconda delle priorità di un'organizzazione, può scegliere di base, NTLM o consentire agli utenti di scegliere tra i due. Se si sceglie solo uno, è preferibile disattivare l'altro dalla directory virtuale del proxy RPC per ridurre il rischio di attacco.
-   **Utilizzare lo stesso set di credenziali per il proxy RPC e il server RPC su HTTP oppure utilizzare credenziali diverse per ciascuno di essi?** Il compromesso per questa decisione è la convenienza e la sicurezza dell'utente. Pochi utenti vogliono immettere più credenziali. Tuttavia, se si verifica una violazione della sicurezza in una rete perimetrale non attendibile, la presenza di set di credenziali separati per il proxy RPC e il server RPC su HTTP forniscono protezione aggiuntiva. Si noti che se vengono utilizzate credenziali separate e un set di credenziali è costituito dalle credenziali di dominio dell'utente, è consigliabile utilizzare le credenziali di dominio dell'utente per il server RPC su HTTP e non per il proxy RPC.

 

 




