---
title: Server proxy e WinRM
description: Windows Gestione remota (WinRM) usa HTTP e HTTPS per inviare messaggi tra i computer client e server. In generale, il client WinRM invia messaggi direttamente al server WinRM. I client WinRM possono anche essere configurati per l'uso di un server proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663493f9c3e71e44be000f436ad4573f911652a8e142b77ffab41acbff250b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112939"
---
# <a name="proxy-servers-and-winrm"></a>Server proxy e WinRM

Windows Gestione remota (WinRM) usa HTTP e HTTPS per inviare messaggi tra i computer client e server. In generale, il client WinRM invia messaggi direttamente al server WinRM. I client WinRM possono anche essere configurati per l'uso di un server proxy.

Per altre informazioni, vedere le sezioni seguenti:

-   [Configurazione di un server proxy per WinRM 2.0](#configuring-a-proxy-server-for-winrm-20)
    -   [Connessioni proxy basate su HTTPS](#https-based-proxy-connections)
    -   [Connessioni proxy basate su HTTP](#http-based-proxy-connections)
-   [Configurazione di un server proxy per WinRM 1.1 e versioni precedenti](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configurazione di un server proxy per WinRM 2.0

WinRM 2.0 supporta un'ampia gamma di configurazioni proxy. WinRM, ad esempio, supporta i proxy per i trasporti HTTP e HTTPS e per i server proxy autenticati e non autenticati.

### <a name="https-based-proxy-connections"></a>HTTPS-Based connessioni proxy

Per migliorare la sicurezza e l'affinità basata sulla connessione, è consigliabile usare HTTPS come meccanismo di trasporto.

Se il server proxy richiede l'autenticazione, i client e i server WinRM devono usare HTTPS.

> [!Note]  
> L'autenticazione al server proxy è indipendente dall'autenticazione al server di destinazione.

 

### <a name="http-based-proxy-connections"></a>HTTP-Based connessioni proxy

Se non è richiesta alcuna autenticazione del server proxy, è possibile usare HTTP o HTTP per il trasporto. Tuttavia, le connessioni basate su HTTP da un client WinRM a un server WinRM tramite un server proxy possono essere problematiche.

Quando si usano connessioni basate su HTTP, è possibile che si verifichino i problemi seguenti:

-   Il server proxy non supporta l'autenticazione basata sulla connessione, che può causare l'esito negativo dell'autenticazione sul server di destinazione con un errore di accesso negato.
-   È necessario più di un set di credenziali per connettersi al server di destinazione e al server proxy.
-   I server proxy basati su HTTP potrebbero non supportare la possibilità di mantenere le connessioni associate basate su client e basate su server. Se il proxy non collega un client a un server e mantiene la connessione TCP/IP, i client non autenticati potrebbero ottenere l'accesso ai dati. Inoltre, la mancanza di affinità di connessione potrebbe causare l'esito negativo dell'autenticazione sul server.

Se è necessario usare HTTP come trasporto, il server proxy deve supportare la configurazione seguente per ottenere una risposta WinRM migliore e per evitare errori di accesso negato per i client WinRM:

-   Supporto per HTTP/1.1. HTTP/1.1 è più stringente nel mapping dell'affinità di connessione tra client e server.
-   Autenticazione basata sulla connessione per l'autenticazione Negotiate, Kerberos e CredSSP.

    L'autenticazione di una richiesta richiede più round trip tra il client e il server. La maggior parte delle negoziazioni per l'autenticazione viene completata dopo che il server di autenticazione (WinRM) invia una risposta al client che non è una risposta 401 (non autorizzata). Se il server Gestione remota Windows restituisce una risposta al client che non è una risposta 401, il proxy non deve chiudere la connessione.

    È possibile inviare più coppie di richiesta/risposta tra client e server prima che i dati effettivi del pacchetto siano inviati. WinRM 2.0 usa gli schemi di autenticazione Negotiate e Kerberos con crittografia, che possono aggiungere round trip aggiuntivi. I dati non possono essere inviati al server fino al completamento dell'autenticazione.

    Il server Gestione remota Windows restituisce una risposta di livello 200 che indica che l'autenticazione è stata completata. I server proxy basati su HTTP potrebbero terminare l'affinità di autenticazione basata sulla connessione e chiudere la connessione TCP/IP dopo aver ricevuto la risposta di livello 200 dal server WinRM. Il round trip finale dal client al server non include il pacchetto di richiesta originale. Se il server proxy chiude la connessione, il server tenterà di autenticare nuovamente il client e la richiesta del client potrebbe non essere mai inviata al server. Se l'affinità basata sulla connessione non viene mantenuta, l'autenticazione nel server di destinazione può non riuscire con un errore di accesso negato.

-   Persistenza della connessione. La connessione TCP/IP del client al proxy deve continuare a eseguire il mapping alla stessa connessione TCP/IP dal proxy al server. La gestione di questa connessione consente di ottenere un livello superiore di prestazioni. Se la connessione non viene mantenuta, ogni richiesta deve essere autenticata nuovamente, con un impatto sulle prestazioni.

### <a name="encryption-and-winrm-20"></a>Crittografia e WinRM 2.0

WinRM 2.0 supporta la crittografia su HTTP usando gli schemi di autenticazione Negotiate, Kerberos e CredSSP. Se un server WinRM supporta HTTP ed è accessibile tramite un proxy, il server WinRM deve applicare la crittografia e non consentire il traffico di rete non crittografato.

In nessun caso le richieste HTTP non crittografate devono essere inviate tramite server proxy. Quando i dati devono passare attraverso un server proxy prima di essere inviati al server di destinazione, i problemi di sicurezza seguenti sono molto importanti:

-   È possibile che un server proxy dannoso possa esaminare ogni coppia richiesta/risposta, incluse le credenziali.
-   Se le connessioni TCP/IP non sono fortemente mappate tra il client WinRM e il server proxy e tra il server proxy e il server di destinazione, un client non autorizzato potrebbe connettersi al server di destinazione usando la stessa connessione autenticata dal server proxy al server di destinazione. Il server di destinazione potrebbe consentire al client non autenticato di accedere ai dati. Se viene applicata la crittografia, il server di destinazione invia un messaggio di accesso negato al client non autenticato.

L'uso della crittografia consente di attenuare questi potenziali problemi di sicurezza.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configurazione di un server proxy per WinRM 1.1 e versioni precedenti

Se è necessario un proxy per raggiungere il server WinRM, il client WinRM si basa sulla configurazione del proxy Windows servizi HTTP (WinHTTP). Per impostazione predefinita, WinHTTP non è configurato per l'uso di un server proxy. La configurazione del proxy WinHTTP può essere modificata usando le [ utilitàProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) o [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) della riga di comando.

**WinRM 1.1 e versioni precedenti:** WinRM non usa le impostazioni Internet Explorer proxy.

 

 