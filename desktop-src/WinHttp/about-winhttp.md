---
description: I servizi HTTP di Microsoft Windows (WinHTTP) forniscono un'interfaccia di alto livello supportata dal server per i protocolli Internet HTTP/2 e 1,1.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Informazioni su WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150c829410a1601a3ede7f115f4594276af7fead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314615"
---
# <a name="about-winhttp"></a>Informazioni su WinHTTP

> [!NOTE]
> Per i contenitori di app e i servizi di sistema da Windows 10, versione 1709, HTTP/2 (vedere [RFC7540](https://tools.ietf.org/html/rfc7540)) è attiva per impostazione predefinita.

I servizi HTTP di Microsoft Windows (WinHTTP) forniscono un'interfaccia di alto livello supportata dal server per i protocolli Internet HTTP/2 e 1,1. WinHTTP è progettato per essere utilizzato principalmente in scenari basati su server da applicazioni server che comunicano con i server HTTP.

[WinInet](/windows/desktop/WinInet/portal) è stato progettato come piattaforma client HTTP per applicazioni desktop interattive. WinINet Visualizza un'interfaccia utente per alcune operazioni, ad esempio la raccolta delle credenziali utente. WinHTTP, tuttavia, gestisce queste operazioni a livello di codice. Le applicazioni server che richiedono servizi client HTTP devono usare WinHTTP anziché WinINet. Per altre informazioni, vedere [porting di applicazioni WinInet a WinHTTP](porting-wininet-applications-to-winhttp.md).

WinHTTP è inoltre progettato per l'utilizzo in servizi di sistema e applicazioni client basate su HTTP. Tuttavia, le applicazioni a utente singolo che richiedono la funzionalità del protocollo FTP, la persistenza dei cookie, la memorizzazione nella cache, la gestione automatica delle finestre di dialogo delle credenziali, la [compatibilità con Internet](/windows/desktop/WinInet/portal)Explorer o il supporto della piattaforma di livello inferiore

Questa interfaccia è accessibile da C/C++ usando il Application Programming Interface WinHTTP (API) o usando le interfacce [**IWinHttpRequest**](iwinhttprequest-interface.md) e [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) . WinHTTP è inoltre accessibile da script e da Microsoft Visual Basic tramite l'oggetto WinHTTP. Per ulteriori informazioni e descrizioni delle singole funzioni, vedere le informazioni di riferimento sulle funzioni WinHTTP per il linguaggio specifico.

A partire da Windows 8, WinHTTP fornisce le API per abilitare le connessioni usando il [protocollo WebSocket](https://tools.ietf.org/html/rfc6455)l, ad esempio [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) e [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> WinHTTP non è rientrante tranne che durante il callback di completamento asincrono. Ovvero, mentre un thread presenta una chiamata in sospeso a una delle funzioni WinHTTP, ad esempio WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData o WinHttpWriteData, non deve mai chiamare WinHTTP una seconda volta fino al completamento della prima chiamata. Uno scenario in cui può verificarsi una seconda chiamata è il seguente: se un'applicazione Accoda una chiamata di procedura asincrona (APC) al thread che chiama WinHTTP e se WinHTTP esegue un'attesa di avviso internamente, è possibile eseguire l'APC. Se la routine APC viene eseguita anche per chiamare WinHTTP, l'API WinHTTP viene nuovamente immessa e lo stato interno di WinHTTP può essere danneggiato.

## <a name="winhttp-51-features"></a>Funzionalità di WinHTTP 5,1

Nella versione 5,1 di WinHTTP sono state aggiunte le funzionalità seguenti:

-   Supporto IPv6.
-   Funzionalità di AutoProxy.
-   Protocollo HTTP/1.0, incluso il supporto per connessioni keep-alive (permanenti) e cookie di sessione.
-   Supporto di trasferimento Chunked HTTP/1.1 per risposte HTTP.
-   Pool Keep-Alive di connessioni anonime tra sessioni.
-   Funzionalità di Secure Sockets Layer (SSL), inclusi i certificati client. I protocolli SSL supportati sono i seguenti: SSL 2,0, SSL 3,0 e Transport Layer Security (TLS) 1,0.
-   Supporto per l'autenticazione server e proxy, incluso il supporto integrato per Microsoft Passport 1,4 e il pacchetto Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md) .
-   Gestione automatica dei reindirizzamenti a meno che non vengano eliminati.
-   Interfaccia di scripting, oltre all'API.
-   Utilità di traccia per facilitare la risoluzione dei problemi.

Una serie di funzionalità [WinInet](/windows/desktop/WinInet/portal) non è supportata in WinHTTP, tra cui la memorizzazione nella cache degli URL e i cookie persistenti, AutoProxy, autodialing, supporto offline e file Transfer Protocol (FTP).

Per ulteriori informazioni sulle modifiche introdotte nella versione 5,1, vedere Novità di [WinHTTP 5,1](what-s-new-in-winhttp-5-1.md).

## <a name="getting-started-with-winhttp"></a>Introduzione con WinHTTP

Per ulteriori informazioni su WinHTTP, vedere gli argomenti seguenti.

* [WinInet rispetto a WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) Confronta le due tecnologie per l'accesso a http.
* Le [versioni WinHTTP](winhttp-versions.md) descrivono la cronologia delle versioni di WinHTTP.
* Novità [di winhttp 5,1](what-s-new-in-winhttp-5-1.md) descrive le modifiche e le nuove funzionalità di WinHTTP 5,1.
* La [terminologia di rete](network-terminology.md) descrive i concetti e la terminologia utili relativi alla rete in generale e al protocollo HTTP in particolare.
* La [scelta di un'interfaccia WinHTTP](choosing-a-winhttp-interface.md) descrive l'API C/C++ e l'interfaccia com per WinHTTP.
* Le [considerazioni sulla sicurezza di WinHTTP](winhttp-security-considerations.md) descrivono i problemi di sicurezza da tenere presenti quando si usa WinHTTP.
* Il [porting di applicazioni WinInet a WinHTTP](porting-wininet-applications-to-winhttp.md) descrive come modificare le applicazioni [WinInet](/windows/desktop/WinInet/portal) esistenti per l'uso dell'API WinHTTP.
