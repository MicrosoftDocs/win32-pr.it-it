---
title: Sicurezza RPC su HTTP
description: RPC su HTTP offre tre tipi di sicurezza oltre alla sicurezza RPC standard, che comporta la protezione una sola volta del traffico RPC su HTTP da RPC e quindi doppiamente protetta dal meccanismo di tunneling fornito da RPC su HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f1ebd5a7198a2b2ccae7703b92011bbd45b037db2f7ef8eb116e28ef06d8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926137"
---
# <a name="rpc-over-http-security"></a>Sicurezza RPC su HTTP

RPC su HTTP offre tre tipi di sicurezza oltre alla sicurezza RPC standard, che comporta la protezione una sola volta del traffico RPC su HTTP da RPC e quindi doppiamente protetta dal meccanismo di tunneling fornito da RPC su HTTP. Per una descrizione dei meccanismi di sicurezza RPC standard, vedere [Sicurezza](security.md). Il meccanismo di tunneling RPC su HTTP aggiunge la normale sicurezza RPC nel modo seguente:

-   Fornisce sicurezza tramite IIS (disponibile solo per RPC su HTTP v2).
-   Fornisce la crittografia SSL e la verifica del proxy RPC (autenticazione reciproca). Disponibile anche solo in RPC su HTTP v2.
-   Fornisce restrizioni a livello di proxy RPC che dettano i computer nella rete del server autorizzati a ricevere chiamate RPC su HTTP.

Ognuna di queste tre funzionalità di sicurezza è descritta in modo più dettagliato nelle sezioni seguenti.

## <a name="iis-authentication"></a>Autenticazione IIS

RPC su HTTP può sfruttare il normale meccanismo di autenticazione di IIS. La directory virtuale per il proxy RPC può essere configurata usando il nodo Rpc nel sito Web predefinito nello snap-in MMC IIS:

![Screenshot che mostra il nodo Rpc nel sito Web predefinito nello snap-in MMC IIS.](images/rpc-http-1.png)

IIS può essere configurato per disabilitare l'accesso anonimo e richiedere l'autenticazione alla directory virtuale per il proxy RPC. A tale scopo, fare clic con il pulsante destro del mouse sul nodo Rpc e scegliere **Proprietà**. Selezionare la **scheda Sicurezza directory** e fare clic sul **pulsante** Modifica nel gruppo Autenticazione e controllo **di** accesso, come illustrato di seguito:

![Screenshot che mostra la finestra di dialogo Proprietà RPC.](images/rpc-http-2.png)

Anche se è possibile usare RPC su HTTP anche quando la directory virtuale proxy RPC consente l'accesso anonimo, Microsoft consiglia di disabilitare l'accesso anonimo a tale directory virtuale per motivi di sicurezza. Invece, per RPC su HTTP abilitare l'autenticazione di base, Windows'autenticazione integrata o entrambi. Tenere presente che solo RPC su HTTP v2 è in grado di eseguire l'autenticazione sul proxy RPC che richiede l'autenticazione di base o Windows integrata; RPC su HTTP v1 non sarà in grado di connettersi se **l'opzione Non consentire l'accesso anonimo** è disabilitata. Poiché RPC su HTTP v2 è l'implementazione più sicura e affidabile, l'uso di una versione di Windows che la supporta migliorerà la sicurezza delle installazioni.

> [!Note]  
> Per impostazione predefinita, la directory virtuale proxy RPC è contrassegnata per consentire l'accesso anonimo. Tuttavia, il proxy RPC per RPC su HTTP v2 rifiuta le richieste non autenticate per impostazione predefinita.

 

## <a name="traffic-encryption"></a>Crittografia del traffico

RPC su HTTP può crittografare il traffico tra il client RPC su HTTP e il proxy RPC con SSL. Il traffico tra il proxy RPC e il server RPC su HTTP viene crittografato usando normali meccanismi di sicurezza RPC e non usa SSL (anche se viene scelto SSL tra il client e il proxy RPC). Ciò è dovuto al fatto che la parte del traffico viaggia all'interno della rete di un'organizzazione e dietro un firewall.

Il traffico tra il client RPC su HTTP e il proxy RPC, che in genere viaggia su Internet, può essere crittografato con SSL oltre al meccanismo di crittografia scelto per RPC. In questo caso, il traffico sulla parte Internet della route diventa doppiamente crittografato. La crittografia del traffico tramite il proxy RPC offre una difesa secondaria, nel caso in cui il proxy RPC o altri computer nella rete perimetrale siano compromessi. Poiché il proxy RPC non è in grado di decrittografare il livello di crittografia secondario, il proxy RPC non ha accesso ai dati inviati. Per [altre informazioni,](rpc-over-http-deployment-recommendations.md) vedere Consigli distribuzione RPC su HTTP. La crittografia SSL è disponibile solo con RPC su HTTP v2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Limitazione delle chiamate RPC su HTTP a determinati computer

La configurazione della sicurezza iis è basata sugli intervalli di computer e porte consentiti. La funzionalità di utilizzo di RPC su HTTP è controllata da due voci del Registro di sistema nel computer che esegue IIS e il proxy RPC. La prima voce è un flag che attiva o disattiva la funzionalità proxy RPC. Il secondo è un elenco facoltativo di computer a cui il proxy può inoltrare chiamate RPC.

Per impostazione predefinita, un client che contatta il proxy RPC per eseguire il tunneling delle chiamate RPC su HTTP non può accedere ad alcun processo del server RPC, ad eccezione dei processi rpc su server HTTP in esecuzione nello stesso computer del proxy RPC. Se il flag ENABLED non è definito o impostato su un valore zero, IIS disabilita il proxy RPC. Se il flag ENABLED è definito e impostato su un valore diverso da zero, un client può connettersi a RPC su server HTTP nel computer che esegue IIS. Per consentire al client di eseguire il tunneling a un processo del server RPC su HTTP in un altro computer, è necessario aggiungere una voce del Registro di sistema all'elenco di server RPC su HTTP del computer IIS.

I server RPC non possono accettare chiamate RPC su HTTP a meno che non siano stati specificamente richiesti rpc per l'ascolto su RPC su HTTP.

L'esempio seguente illustra come configurare il Registro di sistema per consentire ai client di connettersi ai server tramite Internet:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

La **voce ValidPorts** è una voce REG SZ contenente un elenco di computer a cui il proxy RPC IIS può inoltrare le chiamate RPC e le porte che deve usare per connettersi ai server \_ RPC. La voce \_ REG SZ ha il formato seguente: Rosco:593; Rosco:2000-8000;Dati \* :4000-8000.

In questo esempio IIS può inoltrare chiamate RPC su HTTP al server "Rosco" sulle porte da 593 e 2000 a 8000. Può anche inviare chiamate a qualsiasi server il cui nome inizia con "Data". Si connetterà alle porte da 4000 a 8000. Inoltre, prima di inoltrare il traffico a una determinata porta sul server RPC su HTTP, il proxy RPC esegue uno scambio di pacchetti speciale con il servizio RPC in ascolto su tale porta per verificare che sia disposto ad accettare richieste su HTTP.

Per un esempio basato su queste impostazioni di esempio, se un servizio RPC è in ascolto sulla porta 4500 sul server "Data1" ma non ha chiamato una delle funzioni [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) con _*ncacn http**, la richiesta verrà \_ rifiutata. Questo comportamento offre protezione aggiuntiva per i server in ascolto su una porta aperta a causa di un errore di configurazione. a meno che il server non sia specificamente richiesto di restare in ascolto su RPC su HTTP, non riceverà chiamate provenienti dall'esterno del firewall.

Le voci nella chiave **ValidPorts** devono corrispondere esattamente al server RPC su HTTP richiesto dal client (non fa distinzione tra maiuscole e minuscole). Per semplificare l'elaborazione, il proxy RPC non esegue la canonizzazione del nome fornito dal client RPC su HTTP. Pertanto, se il client richiede rosco.microsoft.com e in **ValidPorts** contiene solo Rosco, il proxy RPC non corrisponderà ai nomi, anche se entrambi i nomi possono fare riferimento allo stesso computer. Inoltre, se l'indirizzo IP di Rosco è 66.77.88.99 e il client richiede 66.77.88.99 ma la chiave **ValidPorts** contiene solo Rosco, il proxy RPC rifiuterà la connessione. Se un client può richiedere il server RPC su HTTP in base al nome o all'indirizzo IP, inserire entrambi nella **chiave ValidPorts.**

> [!Note]  
> Sebbene RPC sia abilitato per IPv6, il proxy RPC non supporta gli indirizzi IPv6 nella **chiave ValidPorts.** Se si usa IPv6 per connettere il proxy RPC e il server RPC su HTTP, è possibile usare solo i nomi DNS.

 

IIS legge le voci **del Registro di** sistema Enabled e **ValidPorts** all'avvio. RPC su HTTP rilegge inoltre il contenuto della **chiave ValidPorts** circa ogni 5 minuti. Se la **voce ValidPorts** viene modificata, le modifiche vengono implementate entro 5 minuti.

**RPC su HTTP v1:** Il servizio WEB deve essere arrestato e riavviato usando internet Service Manager per l'implementazione dei nuovi valori nelle voci del Registro di sistema.

 

 




