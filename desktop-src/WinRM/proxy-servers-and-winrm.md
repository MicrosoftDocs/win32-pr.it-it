---
title: Server proxy e WinRM
description: Gestione remota Windows (WinRM) Usa HTTP e HTTPS per inviare messaggi tra i computer client e server. In generale, il client WinRM invia messaggi direttamente al server WinRM. I client WinRM possono inoltre essere configurati per l'utilizzo di un server proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07bbfebb4c8f0eb9e77a8942d54677b55c60006
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727399"
---
# <a name="proxy-servers-and-winrm"></a>Server proxy e WinRM

Gestione remota Windows (WinRM) Usa HTTP e HTTPS per inviare messaggi tra i computer client e server. In generale, il client WinRM invia messaggi direttamente al server WinRM. I client WinRM possono inoltre essere configurati per l'utilizzo di un server proxy.

Per altre informazioni, vedere le sezioni seguenti:

-   [Configurazione di un server proxy per WinRM 2,0](#configuring-a-proxy-server-for-winrm-20)
    -   [Connessioni proxy basate su HTTPS](#https-based-proxy-connections)
    -   [Connessioni proxy basate su HTTP](#http-based-proxy-connections)
-   [Configurazione di un server proxy per WinRM 1,1 e versioni precedenti](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configurazione di un server proxy per WinRM 2,0

WinRM 2,0 supporta un'ampia gamma di configurazioni proxy. Ad esempio, WinRM supporta i proxy per i trasporti HTTP e HTTPS e per i server proxy autenticati e non autenticati.

### <a name="https-based-proxy-connections"></a>Connessioni proxy HTTPS-Based

Per una migliore sicurezza e affinità basata sulla connessione, HTTPS deve essere utilizzato come meccanismo di trasporto.

Se il server proxy richiede l'autenticazione, è necessario che i client e i server WinRM usino HTTPS.

> [!Note]  
> L'autenticazione per il server proxy è indipendente dall'autenticazione al server di destinazione.

 

### <a name="http-based-proxy-connections"></a>Connessioni proxy HTTP-Based

Se non è richiesta l'autenticazione del server proxy, è possibile usare HTTP o HTTPs per il trasporto. Tuttavia, le connessioni basate su HTTP da un client WinRM a un server WinRM tramite un server proxy possono risultare problematiche.

Quando si utilizzano connessioni basate su HTTP, potrebbero verificarsi i problemi seguenti:

-   Il server proxy non supporta l'autenticazione basata sulla connessione, che può impedire l'esecuzione dell'autenticazione nel server di destinazione con un errore di accesso negato.
-   Per la connessione al server di destinazione e al server proxy è necessario disporre di più di un set di credenziali.
-   I server proxy basati su HTTP potrebbero non supportare la capacità di gestire le connessioni basate su client e basate su server associate. Se il proxy non collega fortemente un client a un server e mantiene la connessione TCP/IP, i client non autenticati potrebbero ottenere l'accesso ai dati. Inoltre, la mancanza di affinità di connessione potrebbe causare l'esito negativo dell'autenticazione sul server.

Se è necessario utilizzare HTTP come trasporto, il server proxy deve supportare la configurazione seguente per ottenere una risposta WinRM migliore ed evitare errori di accesso negato per i client WinRM:

-   Supporto per HTTP/1.1. HTTP/1.1 è più rigoroso nel mapping dell'affinità di connessione tra client e server.
-   Autenticazione basata sulla connessione per l'autenticazione Negotiate, Kerberos e CredSSP.

    Per l'autenticazione di una richiesta sono necessari più round trip tra il client e il server. La maggior parte della negoziazione per l'autenticazione è completa dopo che il server di autenticazione (WinRM) Invia una risposta al client che non è una risposta 401 (non autorizzato). Se il server WinRM restituisce una risposta al client che non è una risposta 401, il proxy non deve chiudere la connessione.

    È possibile inviare più coppie di richiesta/risposta tra il client e il server prima che vengano inviati i dati dei pacchetti effettivi. WinRM 2,0 utilizza gli schemi di autenticazione Negotiate e Kerberos con la crittografia, che può aggiungere round trip aggiuntivi. I dati non possono essere inviati al server fino al completamento dell'autenticazione.

    Il server WinRM restituisce una risposta a livello di 200 che indica che l'autenticazione è stata completata. I server proxy basati su HTTP potrebbero terminare l'affinità di autenticazione basata sulla connessione e chiudere la connessione TCP/IP dopo aver ricevuto la risposta a livello di 200 dal server WinRM. Il round trip finale dal client al server non include il pacchetto di richiesta originale. Se il server proxy chiude la connessione, il server tenterà di eseguire di nuovo l'autenticazione del client e la richiesta client potrebbe non essere mai inviata al server. Se l'affinità basata sulla connessione non viene mantenuta, l'autenticazione nel server di destinazione può avere esito negativo con un errore di accesso negato.

-   Persistenza della connessione. La connessione TCP/IP del client al proxy deve continuare a eseguire il mapping alla stessa connessione TCP/IP dal proxy al server. La gestione di questa connessione consente di ottenere un livello di prestazioni superiore. Se la connessione non viene mantenuta, è necessario ripetere l'autenticazione di ogni richiesta, che potrebbe influire sulle prestazioni.

### <a name="encryption-and-winrm-20"></a>Crittografia e WinRM 2,0

WinRM 2,0 supporta la crittografia su HTTP tramite gli schemi di autenticazione Negotiate, Kerberos e CredSSP. Se un server WinRM supporta HTTP ed è accessibile tramite un proxy, il server WinRM deve applicare la crittografia e non consentire il traffico di rete non crittografato.

In nessuna circostanza, le richieste HTTP non crittografate devono essere inviate tramite server proxy. Quando i dati devono passare attraverso un server proxy prima di essere inviati al server di destinazione, sono molto importanti i seguenti problemi di sicurezza:

-   È possibile che un server proxy dannoso possa esaminare ogni coppia richiesta-risposta, incluse le credenziali.
-   Se le connessioni TCP/IP non sono fortemente mappate tra il client WinRM e il server proxy e tra il server proxy e il server di destinazione, un client non autorizzato può connettersi al server di destinazione utilizzando la stessa connessione autenticata dal server proxy al server di destinazione. Il server di destinazione potrebbe consentire al client non autenticato di accedere ai dati. Se la crittografia viene applicata, il server di destinazione Invia un messaggio di accesso negato al client non autenticato.

L'uso della crittografia potrebbe attenuare questi potenziali problemi di sicurezza.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configurazione di un server proxy per WinRM 1,1 e versioni precedenti

Se è necessario un proxy per raggiungere il server WinRM, il client WinRM si affida alla configurazione proxy di servizi HTTP Windows (WinHTTP). Per impostazione predefinita, WinHTTP non è configurato per l'uso di un server proxy. È possibile modificare la configurazione del proxy WinHTTP utilizzando le utilità della riga di comando [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) o [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) .

**WinRM 1,1 e versioni precedenti:** WinRM non utilizza le impostazioni proxy di Internet Explorer.

 

 