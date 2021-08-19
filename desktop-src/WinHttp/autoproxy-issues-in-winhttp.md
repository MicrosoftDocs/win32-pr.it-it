---
description: Quando si usa la funzionalità di proxy automatico WinHTTP, considerare i problemi importanti seguenti.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problemi di AutoProxy in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc07ca7320fee028431ff0d89be78ee0b2dc4bb63e8191386808f0936c8a1518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052089"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problemi di AutoProxy in WinHTTP

Quando si usa la funzionalità di proxy automatico WinHTTP, considerare i problemi importanti seguenti.

## <a name="only-one-proxy-server-is-currently-supported"></a>Attualmente è supportato un solo server proxy

WinHTTP attualmente non supporta le configurazioni proxy che specificano più di un server proxy. Se [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) restituisce una struttura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene un elenco di server proxy, che l'applicazione imposta quindi sull'handle di richiesta usando l'opzione **PROXY WINHTTP \_ \_ OPTION, WinHTTP** usa solo il primo server proxy nell'elenco. Se il server proxy non è accessibile, WinHTTP non esegue il failover in nessuno degli altri server proxy nell'elenco. È l'applicazione a gestire questo caso impostando di nuovo l'opzione **WINHTTP \_ OPTION \_ PROXY** con il server proxy successivo nell'elenco e inviando nuovamente la richiesta.

## <a name="security-risk-mitigation"></a>Mitigazione dei rischi per la sicurezza

L'elaborazione del file di configurazione automatica del proxy richiede l'esecuzione del codice script scaricato. Alcuni problemi di sicurezza da considerare: se il server in cui risiede il file PAC è stato compromesso, è possibile che il codice di script PAC sia dannoso. Di conseguenza, WinHTTP usa le precauzioni seguenti per proteggere il client:

1.  Al codice script non è consentito creare un'istanza ActiveX oggetti . In questo modo si bloccano molte funzionalità potenzialmente pericolose, ad esempio la possibilità di accedere ai file e di eseguire operazioni di I/O di rete.
2.  **Windows Server 2003: **[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delega l'intera elaborazione WPAD a un servizio esterno out-of-process, il servizio di individuazione automatica del proxy Web WinHTTP, che viene eseguito con l'account utente predefinito servizio locale con privilegi insufficienti.

3.  **Windows XP con SP2 e Windows Server 2003:** Non è consentita l'esecuzione di uno script PAC per più di 60 secondi, dopo i quali l'esecuzione dello script viene terminata.

4.  **Windows XP con SP2 e Windows Server 2003:** WinHTTP rifiuta i file PAC di dimensioni superiori a 1 MB. Un file PAC tipico è in genere di dimensioni non superiori a pochi kilobyte.

Tenere presente che l'elaborazione del codice di script PAC richiede l'uso di COM, perché WinHTTP usa Microsoft JScript componente per eseguire lo script. Se WinHTTP non è in grado di delegare l'elaborazione del protocollo WPAD a un servizio esterno di individuazione automatica del proxy Web out-of-process, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) carica il runtime COM all'interno del processo dell'applicazione per la durata della chiamata. Se l'applicazione stessa usa già COM, questo non dovrebbe essere un problema.

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

Il processo di rilevamento automatico può essere lento, possibilmente fino a diversi secondi. Le [**funzioni WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) bloccano le funzioni sincrone. È possibile che un particolare meccanismo di rilevamento automatico (ad esempio DHCP) sia molto più lento dell'altro (ad esempio DNS). Se vengono specificati entrambi i flag di rilevamento automatico **\_ \_ \_ \_ WINHTTP AUTO DETECT TYPE DHCP** e **WINHTTP AUTO DETECT \_ TYPE DNS \_ \_ \_ \_ A,** WinHTTP usa dhcp per primo, in base alla specifica WPAD. Se non viene individuato alcun URL PAC tramite l'emissione di una richiesta DHCP, WinHTTP tenta di individuare il file PAC in un indirizzo DNS noto.

[**WinHttpGetProxyForUrl usa**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) il parametro handle di sessione WinHTTP per memorizzare nella cache il file PAC e i risultati del rilevamento automatico. È meglio usare lo stesso handle di sessione per più **chiamate WinHttpGetProxyForUrl,** se possibile, per evitare il rilevamento ripetuto di URL PAC e il download di file. Il file PAC viene memorizzato nella cache solo in memoria e viene eliminato quando l'applicazione chiude l'handle di sessione.

A causa dell'impatto sulle prestazioni del proxy automatico, è consigliabile che solo le applicazioni client desktop o i servizi usino la funzionalità. Le applicazioni basate su server devono basarsi sull'amministratore del server tramite l'utilità "ProxyCfg.exe".

 

 



