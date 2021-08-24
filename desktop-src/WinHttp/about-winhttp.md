---
description: Microsoft Windows SERVIZI HTTP (WinHTTP) offre un'interfaccia di alto livello supportata dal server per i protocolli Internet HTTP/2 e 1.1.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Informazioni su WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19df8ac8073cfca4fd74fd5d024712cc3fc59c770c3d9ad0ab1386bc0642d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570291"
---
# <a name="about-winhttp"></a>Informazioni su WinHTTP

> [!NOTE]
> Per i contenitori di app e i servizi di sistema Windows 10, la versione 1709, HTTP/2 (vedere [RFC7540)](https://tools.ietf.org/html/rfc7540)è impostata su on per impostazione predefinita.

Microsoft Windows SERVIZI HTTP (WinHTTP) offre un'interfaccia di alto livello supportata dal server per i protocolli Internet HTTP/2 e 1.1. WinHTTP è progettato per essere usato principalmente in scenari basati su server da applicazioni server che comunicano con server HTTP.

[WinINet è](/windows/desktop/WinInet/portal) stato progettato come piattaforma client HTTP per applicazioni desktop interattive. WinINet visualizza un'interfaccia utente per alcune operazioni, ad esempio la raccolta di credenziali utente. WinHTTP, tuttavia, gestisce queste operazioni a livello di codice. Le applicazioni server che richiedono servizi client HTTP devono usare WinHTTP anziché WinINet. Per altre informazioni, vedere [Porting WinINet Applications to WinHTTP](porting-wininet-applications-to-winhttp.md).

WinHTTP è progettato anche per l'uso nei servizi di sistema e nelle applicazioni client basate su HTTP. Tuttavia, le applicazioni a utente singolo che richiedono funzionalità del protocollo FTP, persistenza dei cookie, memorizzazione nella cache, gestione automatica della finestra di dialogo delle credenziali, compatibilità Internet Explorer o supporto della piattaforma di livello inferiore devono prendere in considerazione l'uso di [WinINet](/windows/desktop/WinInet/portal).

Questa interfaccia è accessibile da C/C++ usando l'API (Application Programming Interface) WinHTTP o le interfacce [**IWinHttpRequest**](iwinhttprequest-interface.md) e [**IWinHttpRequestEvents.**](iwinhttprequestevents-interface.md) WinHTTP è accessibile anche dallo script e da Microsoft Visual Basic tramite l'oggetto WinHTTP. Per altre informazioni e descrizioni delle singole funzioni, vedere le informazioni di riferimento sulle funzioni WinHTTP per il linguaggio specifico.

A partire da Windows 8, WinHTTP fornisce API per abilitare le connessioni usando il protocollo [WebSocket](https://tools.ietf.org/html/rfc6455)l, ad esempio [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) e [**WinHttpWebSocketReceive.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)

> [!Caution]  
> WinHTTP non è rientrante se non durante il callback di completamento asincrono. Mentre un thread ha una chiamata in sospeso a una delle funzioni WinHTTP, ad esempio WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData o WinHttpWriteData, non deve mai chiamare WinHTTP una seconda volta fino al completamento della prima chiamata. Uno scenario in cui potrebbe verificarsi una seconda chiamata è il seguente: se un'applicazione accoda una chiamata di procedura asincrona (APC) al thread che chiama in WinHTTP e se WinHTTP esegue un'attesa avviso internamente, il APC può essere eseguito. Se la routine APC viene eseguita anche per chiamare WinHTTP, reentererà l'API WinHTTP e lo stato interno di WinHTTP può essere danneggiato.

## <a name="winhttp-51-features"></a>Funzionalità di WinHTTP 5.1

Nella versione 5.1 di WinHTTP sono state aggiunte le funzionalità seguenti:

-   Supporto IPv6.
-   Funzionalità di AutoProxy.
-   Protocollo HTTP/1.0, incluso il supporto per connessioni keep-alive (persistenti) e cookie di sessione.
-   Supporto del trasferimento in blocchi HTTP/1.1 per le risposte HTTP.
-   Pooling keep-alive di connessioni anonime tra sessioni.
-   Secure Sockets Layer (SSL), inclusi i certificati client. I protocolli SSL supportati includono: SSL 2.0, SSL 3.0 e Transport Layer Security (TLS) 1.0.
-   Supporto per l'autenticazione server e proxy, incluso il supporto integrato per Microsoft Passport 1.4 e il pacchetto [Negotiate/Kerberos.](../com/kerberos-v5-protocol.md)
-   Gestione automatica dei reindirizzamenti, a meno che non venga eliminata.
-   Interfaccia che può essere utilizzata tramite script oltre all'API.
-   Utilità di traccia per la risoluzione dei problemi.

In WinHTTP non sono supportate diverse funzionalità [WinINet,](/windows/desktop/WinInet/portal) tra cui la memorizzazione nella cache degli URL e i cookie permanenti, il proxy automatico, la registrazione automatica, il supporto offline e File Transfer Protocol (FTP).

Per altre informazioni sulle modifiche introdotte nella versione 5.1, vedere [Novità di WinHTTP 5.1.](what-s-new-in-winhttp-5-1.md)

## <a name="getting-started-with-winhttp"></a>Attività iniziali con WinHTTP

Per altre informazioni su WinHTTP, vedere gli argomenti seguenti.

* [WinINet e WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) confrontano le due tecnologie per l'accesso a HTTP.
* [Versioni winHTTP](winhttp-versions.md) descrive la cronologia delle versioni di WinHTTP.
* [Novità di WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) descrive le modifiche e le nuove funzionalità di WinHTTP 5.1.
* [Terminologia di rete](network-terminology.md) descrive concetti e terminologia utili relativi alla rete in generale e al protocollo HTTP in particolare.
* [La scelta di un'interfaccia WinHTTP](choosing-a-winhttp-interface.md) descrive l'API C/C++ e l'interfaccia COM per WinHTTP.
* [Considerazioni sulla sicurezza winHTTP](winhttp-security-considerations.md) descrive i problemi di sicurezza da tenere presenti quando si usa WinHTTP.
* [Il porting di applicazioni WinINet in WinHTTP](porting-wininet-applications-to-winhttp.md) descrive come modificare le applicazioni [WinINet](/windows/desktop/WinInet/portal) esistenti per usare l'API WinHTTP.
