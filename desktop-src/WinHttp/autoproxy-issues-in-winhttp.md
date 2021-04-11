---
description: Quando si usa la funzionalità di AutoProxy WinHTTP, tenere presenti i seguenti problemi importanti.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problemi di proxy AutoProxy in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c6edbf56ec1ffc4dfac930a5d4858429cc6447
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233118"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problemi di proxy AutoProxy in WinHTTP

Quando si usa la funzionalità di AutoProxy WinHTTP, tenere presenti i seguenti problemi importanti.

## <a name="only-one-proxy-server-is-currently-supported"></a>Attualmente è supportato un solo server proxy

WinHTTP attualmente non supporta le configurazioni proxy che specificano più di un server proxy. Se [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) restituisce una struttura di [**\_ \_ informazioni proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) contenente un elenco di server proxy, che l'applicazione imposta quindi sull'handle di richiesta utilizzando l'opzione del **\_ \_ proxy di opzione WinHTTP** , WinHTTP utilizzerà solo il primo server proxy nell'elenco. Se il server proxy non è accessibile, WinHTTP non esegue il failover su nessuno degli altri server proxy presenti nell'elenco. È necessario che l'applicazione gestisca questa situazione impostando di nuovo l'opzione del **\_ \_ proxy dell'opzione WinHTTP** con il server proxy successivo nell'elenco e inviando nuovamente la richiesta.

## <a name="security-risk-mitigation"></a>Mitigazione dei rischi di sicurezza

Per elaborare il file di configurazione automatica del proxy è necessario eseguire il codice dello script scaricato. Considerazioni sulla sicurezza: se il server in cui risiede il file PAC è stato compromesso, è possibile che il codice di script PAC sia dannoso. Di conseguenza, WinHTTP usa le precauzioni seguenti per proteggere il client:

1.  Il codice di script non è in grado di creare un'istanza di oggetti ActiveX. Questo consente di bloccare numerose funzionalità potenzialmente pericolose, ad esempio la possibilità di accedere ai file e di eseguire operazioni di I/O di rete.
2.  * * Windows Server 2003: * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delega l'intera elaborazione WPAD a un servizio esterno al processo esterno, il servizio di individuazione automatica proxy Web WinHTTP, che viene eseguito con l'account utente predefinito servizio locale con privilegi limitati.

3.  **Windows XP con SP2 e Windows Server 2003:** Non è consentito eseguire uno script PAC per più di 60 secondi, dopo il quale l'esecuzione dello script viene terminata.

4.  **Windows XP con SP2 e Windows Server 2003:** WinHTTP rifiuta i file PAC di dimensioni superiori a 1 MB. Un tipico file PAC è in genere di dimensioni non superiori a pochi kilobyte.

Tenere presente che l'elaborazione del codice di script PAC richiede l'uso di COM, perché WinHTTP usa il componente Microsoft JScript per eseguire lo script. Se WinHTTP non è in grado di delegare l'elaborazione del protocollo WPAD a un servizio di rilevamento automatico del proxy Web esterno al processo, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) carica il runtime com all'interno del processo dell'applicazione per la durata della chiamata. Se l'applicazione stessa usa già COM, questo non dovrebbe essere un problema.

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

Il processo di rilevamento automatico può essere lento, probabilmente fino a pochi secondi. Le funzioni [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) sono bloccanti, funzioni sincrone. Potrebbe trattarsi di un meccanismo di rilevamento automatico specifico (ad esempio DHCP) molto più lento rispetto all'altro (ad esempio DNS). Se in entrambi i tipi di rilevamento automatico di WinHTTP sono specificati i flag di rilevamento automatico **\_ \_ \_ \_ DHCP** e WinHTTP, il protocollo WinHTTP USA prima DHCP, in conformità con la specifica WPAD. **\_ \_ \_ \_ \_** Se non viene individuato alcun URL PAC inviando una richiesta DHCP, WinHTTP tenta di individuare il file PAC in un indirizzo DNS noto.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) usa il parametro dell'handle di sessione WinHTTP per la memorizzazione nella cache del file PAC e i risultati del rilevamento automatico. È preferibile usare lo stesso handle di sessione per più chiamate **WinHttpGetProxyForUrl** , se possibile, per evitare il rilevamento e il download di file di URL PAC ripetuti. Il file PAC viene memorizzato nella cache solo in memoria e viene rimosso quando l'applicazione chiude l'handle di sessione.

A causa dell'effetto sulle prestazioni di AutoProxy, è consigliabile usare la funzionalità solo per le applicazioni client desktop o per i servizi. le applicazioni basate su server devono basarsi sull'amministratore del server utilizzando l'utilità "ProxyCfg.exe".

 

 



