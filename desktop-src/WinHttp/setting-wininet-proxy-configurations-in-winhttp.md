---
description: Le applicazioni che esereranno la porta da WinINet a WinHTTP potrebbero dover usare le stesse impostazioni del proxy automatico che possono recuperare in WinINet o Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Impostazione delle configurazioni del proxy WinINet in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa060d24036a02752a5eefacc9ea6672dec9bb77bad30f653c8f382490a487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133054"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Impostazione delle configurazioni del proxy WinINet in WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Impostazione del proxy automatico in WinHTTP 5.1

Le applicazioni che esereranno la porta da WinINet a WinHTTP potrebbero dover usare le stesse impostazioni del proxy automatico che possono recuperare in WinINet o Internet Explorer (IE). L'API WinHTTP versione 5.1 può recuperare e usare queste impostazioni proxy. In generale, WinHTTP specifica i server proxy e proxy bypass per sessione quando viene creata la sessione. Queste impostazioni possono essere sostituite per ogni richiesta.

Per usare la stessa configurazione proxy di WinINet o IE, il client WinHTTP deve impostare le impostazioni proxy per la sessione. Inoltre, se IE o WinINet sono configurati per l'uso dell'individuazione automatica del proxy Web (WPAD), il client WinHTTP che usa tali impostazioni deve impostare le impostazioni proxy per ogni richiesta. Le sezioni seguenti descrivono come specificare le impostazioni proxy per una sessione e una richiesta:

-   [Impostazione della configurazione del proxy in una sessione](#setting-the-proxy-configuration-on-a-session)
-   [Impostazione della configurazione del proxy in una singola richiesta](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Impostazione della configurazione del proxy in una sessione

## <a name="the-application-is-running-on-a-user-account"></a>L'applicazione è in esecuzione in un account utente

Prima della creazione di una sessione, l'applicazione chiama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per ottenere le impostazioni proxy di IE. Per ottenere queste impostazioni, l'applicazione deve essere in esecuzione come account utente. Il *parametro pProxyConfig* è un puntatore a una struttura [**WINHTTP CURRENT USER \_ \_ \_ \_ IE PROXY \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) che contiene il nome proxy (*lpszProxy*) e i server proxy bypass (*lpszProxyBypass*). Il nome proxy e i valori di bypass proxy della struttura **WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG** vengono quindi usati per inizializzare la sessione WinHTTP. La sessione viene inizializzata chiamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con i parametri *pwszProxyName* e *pwszProxyBypass* ottenuti dai membri **lpszProxy** e **lpszProxyBypass** della struttura **WINHTTP \_ CURRENT USER \_ \_ \_ IE PROXY \_ CONFIG.**

## <a name="the-application-is-running-as-a-service"></a>L'applicazione è in esecuzione come servizio

L'applicazione deve assicurarsi che le impostazioni del Registro di sistema per un singolo utente siano caricate nel Registro di sistema prima di chiamare [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) Se queste impostazioni non vengono caricate nel Registro di sistema, **WinHttpGetIEProxyConfigForCurrentUser** non può ottenere le impostazioni proxy. Le impostazioni del Registro di sistema per un singolo utente possono essere caricate nel Registro di sistema chiamando la **funzione LoadUserProfile.** Se il caricamento delle impostazioni del Registro di sistema dell'utente non è un'opzione, l'applicazione può chiamare [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con il **\_ \_ \_ \_ PROXY PREDEFINITO** DEL TIPO DI ACCESSO WINHTTP specificato nel *parametro dwAcessType.* Se si specifica il proxy predefinito nella chiamata a **WinHttpOpen,** l'API WinHTTP recupera il set di configurazione del proxy usando l'proxycfg.exe [**WinHTTP.**](proxycfg-exe--a-proxy-configuration-tool.md) Dopo aver caricato le impostazioni del Registro di sistema per un singolo utente, l'applicazione segue i passaggi descritti in L'applicazione è in esecuzione in un [account](#the-application-is-running-on-a-user-account) utente per impostare il nome del proxy e i server proxy bypass.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Impostazione della configurazione del proxy in una singola richiesta

Prima della creazione della sessione, l'applicazione chiama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) per determinare se WinINet e IE sono configurati per l'uso di WPAD. **WinHttpGetIEProxyConfigForCurrentUser** restituisce la struttura [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) che contiene il **membro fAutoDetect.** Il valore **TRUE per** questo membro indica che viene usato WPAD e che il membro **lpszAutoConfigUrl** contiene l'URL WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>Viene usata la configurazione automatica del proxy

Se si usa WPAD, l'applicazione chiama [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per recuperare il proxy per la richiesta. Il *parametro lpwszUrl* contiene l'URL a cui viene inviata la richiesta e il *parametro pAutoProxyOptions* contiene un puntatore alla struttura ([**WINHTTP \_ AUTOPROXY \_ OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) che contiene le opzioni del proxy automatico. L'applicazione inizializza la struttura **WINHTTP \_ AUTOPROXY \_ OPTIONS** con le impostazioni restituite dalla struttura [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) nella chiamata a [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) Il flag **\_ \_ \_ WINHTTP AUTOPROXY CONFIG URL** è specificato nel membro **dwFlags** della struttura **WINHTTP \_ AUTOPROXY \_ OPTIONS** e il membro **lpszAutoconfigUrl** contiene l'URL di configurazione automatica del proxy dalla struttura **WINHTTP CURRENT USER \_ \_ \_ IE PROXY \_ \_ CONFIG.** La **funzione WinHttpGetProxyForUrl** restituisce il nome del proxy e l'elenco di bypass del proxy nei membri **lpszProxy** e **lpszProxyBypass** della struttura [**WINHTTP PROXY \_ \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)

Dopo che il proxy per la richiesta è stato ottenuto [**da WinHttpGetProxyForUrl,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)l'applicazione crea la richiesta [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) Viene [**quindi chiamato WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare il proxy per la richiesta specificando l'handle della richiesta nel *parametro hInternet.* Il *parametro dwOption* nella chiamata a **WinHttpSetOption** deve essere impostato su **WINHTTP OPTION \_ \_ PROXY** e il *parametro lpBuffer* è un puntatore a una struttura [**WINHTTP PROXY \_ \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene il proxy e il bypass proxy da usare per la richiesta.

## <a name="automatic-proxy-configuration-is-not-used"></a>La configurazione automatica del proxy non viene usata

Se la chiamata a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indica che il proxy automatico non viene usato, l'applicazione può semplicemente creare la richiesta [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) La configurazione del proxy è la stessa per l'intera sessione e le modifiche per richiesta non sono necessarie.

 

 



