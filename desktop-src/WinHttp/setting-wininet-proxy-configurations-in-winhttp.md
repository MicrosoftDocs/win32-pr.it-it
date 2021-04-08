---
description: È possibile che le applicazioni che portano da WinINet a WinHTTP debbano usare le stesse impostazioni del proxy AutoProxy che possono recuperare in WinINet o Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Impostazione delle configurazioni del proxy WinINet in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968550"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Impostazione delle configurazioni del proxy WinINet in WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Impostazione del proxy automatico in WinHTTP 5,1

È possibile che le applicazioni che portano da WinINet a WinHTTP debbano usare le stesse impostazioni del proxy AutoProxy che possono recuperare in WinINet o Internet Explorer (IE). L'API WinHTTP versione 5,1 può recuperare e usare queste impostazioni proxy. In generale, WinHTTP specifica il proxy e i server di bypass proxy per ogni singola sessione al momento della creazione della sessione. È possibile eseguire l'override di queste impostazioni in base alle singole richieste.

Per usare la stessa configurazione proxy di WinINet o IE, il client WinHTTP deve impostare le impostazioni proxy per la sessione. Inoltre, se IE o WinINet sono configurati per l'utilizzo del protocollo WPAD (Web Proxy Auto-Discovery), il client WinHTTP che utilizza tali impostazioni deve impostare le impostazioni proxy per ogni singola richiesta. Le sezioni seguenti descrivono come specificare le impostazioni proxy per una sessione e una richiesta:

-   [Impostazione della configurazione del proxy in una sessione](#setting-the-proxy-configuration-on-a-session)
-   [Impostazione della configurazione del proxy su una singola richiesta](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Impostazione della configurazione del proxy in una sessione

## <a name="the-application-is-running-on-a-user-account"></a>L'applicazione è in esecuzione in un account utente

Prima di creare una sessione, l'applicazione chiama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per ottenere le impostazioni del proxy IE. Per ottenere queste impostazioni, l'applicazione deve essere in esecuzione come account utente. Il *parametro pProxyConfig* è un puntatore a una struttura di configurazione del [**\_ \_ \_ \_ proxy \_ di Internet Explorer dell'utente corrente WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) che contiene i server proxy Name (*lpszProxy*) e proxy bypass (*lpszProxyBypass*). Il nome proxy e i valori di bypass proxy della struttura di **configurazione del proxy di \_ \_ IE dell'utente \_ \_ \_ corrente WinHTTP** vengono quindi utilizzati per inizializzare la sessione WinHTTP. La sessione viene inizializzata chiamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con i parametri *pwszProxyName* e *PwszProxyBypass* ottenuti dai membri **lpszProxy** e **lpszProxyBypass** della struttura **di \_ \_ configurazione del \_ \_ proxy di \_ Internet Explorer dell'utente corrente WinHTTP** .

## <a name="the-application-is-running-as-a-service"></a>L'applicazione è in esecuzione come servizio

L'applicazione deve assicurarsi che le impostazioni del registro di sistema per un singolo utente vengano caricate nel registro di sistema prima di chiamare [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Se queste impostazioni non vengono caricate nel registro di sistema, **WinHttpGetIEProxyConfigForCurrentUser** non è in grado di ottenere le impostazioni del proxy. Le impostazioni del registro di sistema per un singolo utente possono essere caricate nel registro di sistema chiamando la funzione **LoadUserProfile** . Se il caricamento delle impostazioni del registro di sistema dell'utente non è un'opzione, l'applicazione può chiamare [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con il **\_ \_ \_ \_ proxy predefinito del tipo di accesso WinHTTP** specificato nel parametro *dwAcessType* . Se si specifica il proxy predefinito nella chiamata a **WinHttpOpen** , l'API WinHTTP recupererà il set di configurazione proxy utilizzando l'utilità WinHTTP [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) . Una volta caricate le impostazioni del registro di sistema per un singolo utente, l'applicazione segue i passaggi descritti in [esecuzione dell'applicazione in un account utente](#the-application-is-running-on-a-user-account) per impostare il nome proxy e i server proxy bypass.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Impostazione della configurazione del proxy su una singola richiesta

Prima della creazione della sessione, l'applicazione chiama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per determinare se WinInet e IE sono configurati per l'uso di WPAD. **WinHttpGetIEProxyConfigForCurrentUser** restituisce la struttura di [**\_ configurazione del \_ \_ \_ proxy \_ di Internet Explorer dell'utente corrente WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) che contiene il membro **fAutoDetect** . Il valore **true** per questo membro indica che viene utilizzato WPAD e il membro **LPSZAUTOCONFIGURL** contiene l'URL WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>Viene utilizzata la configurazione automatica del proxy

Se si utilizza WPAD, l'applicazione chiama [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per recuperare il proxy per la richiesta. Il parametro *lpwszUrl* contiene l'URL a cui viene inviata la richiesta e il parametro *pAutoProxyOptions* contiene un puntatore alla struttura ([**\_ \_ Opzioni del proxy AutoProxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) che contiene le opzioni del proxy AutoProxy. L'applicazione Inizializza la struttura delle **\_ \_ Opzioni del proxy AutoProxy WinHTTP** con le impostazioni restituite dalla struttura di [**configurazione del \_ \_ \_ \_ proxy \_ di Internet Explorer dell'utente corrente WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) nella chiamata a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Il **flag \_ \_ \_ URL di configurazione AutoProxy WinHTTP** viene specificato nel **membro DWFLAGS** della struttura **delle \_ \_ Opzioni del proxy automatico WinHTTP** e il membro **lpszAutoconfigUrl** contiene l'URL di configurazione automatica del proxy dalla struttura di configurazione del **\_ \_ \_ \_ proxy \_ di Internet Explorer dell'utente corrente WinHTTP** . La funzione **WinHttpGetProxyForUrl** restituisce il nome del proxy e l'elenco proxy bypass nei membri **lpszProxy** e **lpszProxyBypass** della struttura [**di \_ \_ informazioni del proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) .

Dopo che il proxy per la richiesta è stato ottenuto da [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), l'applicazione crea la richiesta con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Viene quindi chiamato [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare il proxy per la richiesta specificando l'handle di richiesta nel parametro *HINTERNET* . Il parametro *dwOption* nella chiamata a **WinHttpSetOption** deve essere impostato sul **\_ \_ proxy di opzione WinHTTP** e il parametro *lpBuffer* è un puntatore a una struttura di [**\_ \_ informazioni proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene il proxy e il bypass del proxy da usare per la richiesta.

## <a name="automatic-proxy-configuration-is-not-used"></a>La configurazione automatica del proxy non viene utilizzata

Se la chiamata a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indica che non viene usato AutoProxy, l'applicazione può semplicemente creare la richiesta con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). La configurazione del proxy è la stessa per l'intera sessione e le modifiche per richiesta non sono necessarie.

 

 



