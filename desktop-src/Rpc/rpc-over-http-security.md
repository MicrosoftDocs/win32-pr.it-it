---
title: Sicurezza RPC su HTTP
description: In RPC su HTTP sono disponibili tre tipi di sicurezza, oltre alla sicurezza RPC standard, il che comporta il traffico RPC su HTTP protetto una sola volta da RPC, quindi doppiamente protetto dal meccanismo di tunneling fornito da RPC su HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527cf5ff74120c41606d83a248e355a6ea46d9d5
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104234453"
---
# <a name="rpc-over-http-security"></a>Sicurezza RPC su HTTP

In RPC su HTTP sono disponibili tre tipi di sicurezza, oltre alla sicurezza RPC standard, il che comporta il traffico RPC su HTTP protetto una sola volta da RPC, quindi doppiamente protetto dal meccanismo di tunneling fornito da RPC su HTTP. Per una descrizione dei meccanismi di sicurezza RPC standard, vedere [sicurezza](security.md). Il meccanismo di tunneling RPC su HTTP consente di aggiungere alla sicurezza RPC normale nel modo seguente:

-   Fornisce sicurezza attraverso IIS (disponibile solo per RPC su HTTP v2).
-   Fornisce la crittografia SSL e la verifica del proxy RPC (autenticazione reciproca). Disponibile anche in RPC solo su HTTP V2.
-   Fornisce restrizioni sul livello del proxy RPC che stabilisce quali computer della rete server sono autorizzati a ricevere chiamate RPC su chiamate HTTP.

Ognuna di queste tre funzionalità di sicurezza è descritta in modo più dettagliato nelle sezioni seguenti.

## <a name="iis-authentication"></a>Autenticazione IIS

RPC su HTTP può sfruttare il normale meccanismo di autenticazione di IIS. La directory virtuale per il proxy RPC può essere configurata utilizzando il nodo RPC nel sito Web predefinito nello snap-in MMC IIS:

![Screenshot che mostra il nodo RPC nel sito Web predefinito nello snap-in MMC di IIS.](images/rpc-http-1.png)

IIS può essere configurato per disabilitare l'accesso anonimo e richiedere l'autenticazione alla directory virtuale per il proxy RPC. A tale scopo, fare clic con il pulsante destro del mouse sul nodo RPC e scegliere **Proprietà**. Selezionare la scheda **sicurezza directory** e fare clic sul pulsante **modifica** nel gruppo **controllo autenticazione e accesso** , come illustrato di seguito:

![Screenshot che mostra la finestra di dialogo Proprietà RPC.](images/rpc-http-2.png)

Sebbene sia possibile utilizzare RPC su HTTP anche quando la directory virtuale del proxy RPC consente l'accesso anonimo, Microsoft consiglia vivamente di disabilitare l'accesso anonimo alla directory virtuale per motivi di sicurezza. Per RPC su HTTP è invece abilitata l'autenticazione di base, l'autenticazione integrata di Windows o entrambi. Tenere presente che solo RPC su HTTP V2 è in grado di eseguire l'autenticazione con il proxy RPC che richiede l'autenticazione di base o integrata di Windows. RPC su HTTP V1 non sarà in grado di connettersi se non **consentire l'accesso anonimo** è disabilitato. Poiché RPC su HTTP V2 è l'implementazione più sicura e affidabile, l'uso di una versione di Windows che lo supporta consente di migliorare la sicurezza delle installazioni.

> [!Note]  
> Per impostazione predefinita, la directory virtuale del proxy RPC è contrassegnata per consentire l'accesso anonimo. Tuttavia, il proxy RPC per RPC su HTTP V2 rifiuta le richieste non autenticate per impostazione predefinita.

 

## <a name="traffic-encryption"></a>Crittografia del traffico

RPC su HTTP può crittografare il traffico tra il client RPC su HTTP e il proxy RPC con SSL. Il traffico tra il proxy RPC e il server RPC su HTTP viene crittografato utilizzando i normali meccanismi di sicurezza RPC e non utilizza SSL (anche se viene scelto SSL tra il client e il proxy RPC). Questo è dovuto al fatto che la parte del traffico viene spostata all'interno della rete di un'organizzazione e dietro a un firewall.

Il traffico tra il client RPC su HTTP e il proxy RPC, che in genere si sposta su Internet, può essere crittografato con SSL oltre al meccanismo di crittografia scelto per RPC. In questo caso, il traffico sulla parte Internet della route diventa doppiamente crittografato. La crittografia del traffico tramite il proxy RPC fornisce una difesa secondaria, nel caso in cui il proxy RPC o altri computer nella rete perimetrale siano compromessi. Poiché il proxy RPC non è in grado di decrittografare il livello di crittografia secondario, il proxy RPC non ha accesso ai dati inviati. Per ulteriori informazioni, vedere la pagina relativa ai [consigli sulla distribuzione RPC su http](rpc-over-http-deployment-recommendations.md) . La crittografia SSL è disponibile solo con RPC su HTTP V2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Limitazione delle chiamate RPC su HTTP a determinati computer

La configurazione della sicurezza di IIS è basata sugli intervalli di porte e computer consentiti. La possibilità di usare RPC su HTTP viene controllata da due voci del registro di sistema nel computer che esegue IIS e il proxy RPC. La prima voce è un flag che consente di disabilitare la funzionalità del proxy RPC. Il secondo è un elenco facoltativo dei computer a cui il proxy può eseguire l'inoltro delle chiamate RPC.

Per impostazione predefinita, un client che contatta il proxy RPC per eseguire il tunneling di chiamate RPC su HTTP non è in grado di accedere ai processi del server RPC ad eccezione dei processi del server RPC su HTTP in esecuzione nello stesso computer del proxy RPC. Se il flag ENABLED non è definito o è impostato su un valore pari a zero, il proxy RPC viene disabilitato da IIS. Se il flag ENABLED viene definito e impostato su un valore diverso da zero, un client può connettersi a RPC su server HTTP nel computer che esegue IIS. Per consentire al client di effettuare il tunneling a un processo server RPC su HTTP in un altro computer, è necessario aggiungere una voce del registro di sistema all'elenco dei server RPC su HTTP del computer IIS.

I server RPC non accettano RPC su chiamate HTTP, a meno che non abbia richiesto in modo specifico la chiamata RPC per l'ascolto su RPC su HTTP.

Nell'esempio seguente viene illustrato come configurare il registro di sistema per consentire ai client di connettersi ai server su Internet:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

La voce **ValidPorts** è una \_ voce reg SZ contenente un elenco di computer a cui il proxy RPC IIS è autorizzato a eseguire l'inoltro delle chiamate RPC e le porte da utilizzare per connettersi ai server RPC. La \_ voce reg SZ assume il formato seguente: Rosco: 593; Rosco: 2000-8000; dati \* : 4000-8000.

In questo esempio, IIS è in grado di eseguire la trasmissione RPC su chiamate HTTP al server "Rosco" sulle porte 593 e 2000 a 8000. Può anche inviare chiamate a qualsiasi server il cui nome inizia con "data". Si connetterà sulle porte da 4000 a 8000. Inoltre, prima di eseguire l'inoltro del traffico a una determinata porta sul server RPC su HTTP, il proxy RPC esegue uno speciale scambio di pacchetti con il servizio RPC in ascolto su tale porta per verificare che sia pronto ad accettare le richieste tramite HTTP.

Per un esempio basato su queste impostazioni di esempio, se un servizio RPC è in ascolto sulla porta 4500 sul server "Data1", ma non ha chiamato una delle funzioni [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) con _ * ncacn \_ http * *, rifiuterà la richiesta. Questo comportamento fornisce protezione aggiuntiva per i server che restano in attesa su una porta aperta a causa di un errore di configurazione. a meno che il server non abbia richiesto in modo specifico di restare in ascolto su RPC su HTTP, non riceverà chiamate provenienti dall'esterno del firewall.

Le voci nella chiave **ValidPorts** devono corrispondere esattamente a quelle del server RPC su http richiesto dal client (senza distinzione tra maiuscole e minuscole). Per semplificare l'elaborazione, il proxy RPC non esegue la canonizzazione del nome fornito dal client RPC su HTTP. Pertanto, se il client richiede rosco.microsoft.com e in **ValidPorts** contengono solo Rosco, il proxy RPC non corrisponderà ai nomi, anche se entrambi i nomi possono fare riferimento allo stesso computer. Inoltre, se l'indirizzo IP di Rosco è 66.77.88.99 e il client richiede 66.77.88.99 ma la chiave **ValidPorts** contiene solo Rosco, il proxy RPC rifiuterà la connessione. Se un client può richiedere il server RPC su HTTP in base al nome o all'indirizzo IP, inserire entrambi nella chiave **ValidPorts** .

> [!Note]  
> Sebbene RPC sia abilitato per IPv6, il proxy RPC non supporta gli indirizzi IPv6 nella chiave **ValidPorts** . Se si utilizza IPv6 per connettere il proxy RPC e il server RPC su HTTP, è possibile utilizzare solo nomi DNS.

 

IIS legge le voci del registro di sistema **Enabled** e **ValidPorts** all'avvio. Inoltre, RPC su HTTP rilegge il contenuto della chiave **ValidPorts** approssimativamente ogni 5 minuti. Se la voce **ValidPorts** viene modificata, le modifiche verranno implementate entro 5 minuti.

**RPC su http V1:** Il servizio WEB deve essere arrestato e riavviato utilizzando Internet Service Manager per i nuovi valori nelle voci del registro di sistema da implementare.

 

 




