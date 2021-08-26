---
description: Questo argomento illustra l'uso dello strumento di configurazione proxy servizi HTTP di Microsoft Windows (WinHTTP), &\# 0034;ProxyCfg.exe&\# 0034;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe proxy ProxyCfg.exe e Strumenti di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64c952db59fb4709614c498b4d9c732403798e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885830"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe proxy ProxyCfg.exe e Strumenti di configurazione

**Windows Vista e Windows Server 2008: **

ProxyCfg.exe è stato deprecato. Viene sostituito dai comandi [Netsh.exe winhttp.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10))

Questo argomento illustra l'uso dello strumento di configurazione proxy di Servizi HTTP di [Microsoft Windows (WinHTTP),](about-winhttp.md) "ProxyCfg.exe".

Esistono due modi per accedere ai server HTTP e Secure Hypertext Transfer Protocol (HTTPS) tramite un proxy usando Microsoft Windows HTTP Services (WinHTTP). In primo luogo, è possibile specificare le impostazioni proxy dall'interno dell'applicazione WinHTTP. In secondo momento, è possibile specificare le impostazioni proxy predefinite dall'esterno dell'applicazione usando l'utilità di configurazione del proxy disponibile nella directory %windir% \\ system32.

È possibile impostare a livello di codice i dati del proxy dall'interno dell'applicazione o dello script. Se si scrive un'applicazione usando l'API WinHTTP, usare una delle due tecniche seguenti per modificare le impostazioni proxy.

-   Usare la [**funzione WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) Specificare il tipo di accesso nel secondo parametro, il nome del proxy nel terzo parametro e un elenco di bypass nel quarto parametro. L'esempio seguente illustra come usare [**la funzione WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) per impostare i dati proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Usare la [**funzione WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Il flag [**\_ \_ PROXY OPTION WINHTTP**](option-flags.md) consente di specificare le impostazioni proxy con una [**struttura WINHTTP \_ PROXY \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) Il codice di esempio seguente illustra come usare [**la funzione WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare i dati proxy.

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

Se stai scrivendo uno script o un'applicazione usando [**l'oggetto WinHttpRequest,**](winhttprequest.md) usa la tecnica seguente per modificare le impostazioni proxy.

-   Usare il [**metodo SetProxy.**](iwinhttprequest-setproxy.md) Specificare il tipo di accesso nel primo parametro, il nome del proxy nel secondo parametro e un elenco di bypass nel terzo parametro. L'esempio seguente illustra come usare [**il metodo SetProxy**](iwinhttprequest-setproxy.md) nello script per impostare i dati del proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Per specificare le impostazioni predefinite ed eliminare la necessità di usare il [**metodo SetProxy**](iwinhttprequest-setproxy.md) o la [**funzione WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usare l'utilità di configurazione del proxy. Questa utilità consente di specificare che l'applicazione deve accedere a una rete direttamente, tramite un proxy o tramite una combinazione di accesso diretto e proxy specificando un elenco di bypass. Quando si usa l'API WinHTTP, lo strumento di configurazione del proxy determina le impostazioni solo quando si passa il flag **WINHTTP \_ ACCESS TYPE \_ \_ DEFAULT** all'API [**WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**L'oggetto WinHttpRequest**](winhttprequest.md) usa le impostazioni dello strumento di configurazione proxy per impostazione predefinita.

Le impostazioni proxy per WinHTTP non sono le impostazioni proxy per Microsoft Internet Explorer. Non è possibile configurare le impostazioni proxy per WinHTTP nel Windows Pannello di controllo Microsoft. L'uso dell'utilità di configurazione del proxy WinHTTP non modifica le impostazioni usate per Internet Explorer.

> [!Note]  
> Se si tenta di aprire e inviare una richiesta HTTP usando WinHTTP e le impostazioni proxy non sono corrette, si verifica un errore.

 

## <a name="command-line-parameters"></a>Parametri della riga di comando

Nella tabella seguente sono elencati i parametri della riga di comando disponibili per l'uso con lo ProxyCfg.exe seguente.



| Parametro | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno      | Quando non viene specificato alcun parametro, vengono visualizzate le impostazioni proxy WinHTTP correnti.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Vengono visualizzate le informazioni della Guida.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Specifica che le applicazioni WinHTTP accedono direttamente alla rete, senza un proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Specifica il server proxy. È anche possibile specificare un elenco facoltativo di server a cui si accede senza un proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Specifica che le applicazioni WinHTTP usano le impostazioni proxy dell'utente corrente per Internet Explorer. Questo parametro non funziona se Internet Explorer rileva automaticamente le impostazioni proxy o se usa un URL di configurazione automatica per impostare le informazioni del proxy.                                                                                                                                                      |
| i         | Specifica che le applicazioni WinHTTP usano le impostazioni proxy dell'utente corrente per Internet Explorer. Questa operazione funziona solo quando ProxyCfg.exe non è stato usato in precedenza. Se ProxyCfg.exe installato, specificare che il parametro della riga di comando "u" userà le impostazioni manuali. Questo parametro non funziona se Internet Explorer rileva automaticamente le impostazioni proxy o se usa un URL di configurazione automatica per impostare le informazioni del proxy. |



 

È possibile specificare proxy in una stringa delimitata da spazi. Gli elenchi di proxy possono contenere il numero di porta usato per accedere al proxy. Per elencare un proxy per un protocollo specifico, la stringa deve seguire il formato &lt; protocollo &gt; =https://<nome proxy \_>. I protocolli validi sono HTTP e HTTPS. Ad esempio, per elencare un proxy HTTP, una stringa valida è http= , dove nome proxy HTTP è il nome del server proxy e https://http\_proxy\_name:80 80 è il numero di porta che è necessario usare per accedere al \_ \_ proxy. Se il proxy usa il numero di porta predefinito per tale protocollo, è possibile omettere il numero di porta. Se un nome proxy è elencato da solo, è possibile usarlo come proxy predefinito per tutti i protocolli che non dispongono di un proxy specificato. Ad esempio, http= altro proxy usa il proxy HTTP per qualsiasi operazione HTTP, mentre il https://http\_proxy protocollo HTTPS usa il proxy denominato altro \_ \_ \_ proxy.

È possibile elencare i nomi host o gli indirizzi IP noti in locale nell'elenco di bypass del proxy. Questo elenco può contenere caratteri jolly, ad esempio " ", che causano il bypass del server proxy da parte dell'applicazione per gli indirizzi che rientrano nel modello specificato, ad esempio \* " \* .microsoft.com" o " \* .org". I caratteri jolly devono essere i caratteri più a sinistra nell'elenco. Ad esempio, "aaa. \* " non è supportato. Per elencare più indirizzi e nomi host, separarli con spazi vuoti o punti e virgola nella stringa proxy bypass. Se si specifica la &lt; &gt; macro locale, la funzione ignora qualsiasi nome host che non contiene un punto.

> [!WARNING]
> Dopo Proxycfg.exe, non è possibile ripristinare le impostazioni proxy precedenti. Tuttavia, è possibile rimuovere completamente le impostazioni proxy.

 

## <a name="usage"></a>Utilizzo

Per usare lo strumento di configurazione del proxy, aprire una finestra del prompt dei comandi ed eseguire l'utilità di configurazione del proxy con i parametri della riga di comando appropriati. Nella sezione seguente vengono forniti esempi di sintassi.

## <a name="example-syntax"></a>Sintassi di esempio

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Esempio 1: Usare un proxy solo per le risorse esterne

Di seguito è riportato l'uso più comune per Proxycfg.exe. Questo comando specifica che l'accesso ai server HTTP e HTTPS avviene tramite il server proxy denominato "server proxy", ad eccezione dei nomi host che non \_ contengono un punto.

**proxycfg -p server proxy \_ " &lt; local &gt; "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Esempio 2: Usare un proxy per tutte le risorse

Nell'esempio seguente viene specificato che l'accesso ai server HTTP e HTTPS viene eseguito tramite il server proxy denominato "server \_ proxy". Non è specificato alcun elenco di bypass.

**proxycfg -p server proxy \_**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Esempio 3: Usare un proxy diverso per proteggere le risorse

L'esempio seguente specifica che l'accesso ai server HTTP avviene tramite il proxy HTTP e ai \_ server HTTPS tramite il proxy \_ HTTPS. I siti Intranet locali e qualsiasi sito nel dominio \* .microsoft.com ignorano il proxy.

**proxycfg -p "http=http \_ proxy https=https \_ proxy" " local &lt; ; &gt; \* . microsoft.com"**

## <a name="removing-proxycfgexe"></a>Rimozione di ProxyCfg.exe

Dopo aver utilizzato lo strumento di configurazione del proxy, non è possibile ripristinare le impostazioni proxy originali. Se necessario, tuttavia, è possibile rimuovere le impostazioni del Registro di sistema create dall'utilità. Per rimuovere le voci del Registro di sistema ProxyCfg.exe, è necessario eliminare il **valore WinHttpSettings** dalla chiave del Registro di sistema seguente.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Impostazioni** \\ **Connections** \\ **WinHttpSettings**

L'eliminazione *del valore WinHttpSettings* rimuove tutte le configurazioni proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe e autenticazione

L'utilità di configurazione del proxy imposta i criteri di autenticazione predefiniti. Poiché non è consigliabile eseguire l'autenticazione NTLM con host non attendibili, per impostazione predefinita l'autenticazione NTLM viene eseguita automaticamente solo con gli host nell'elenco di bypass del proxy. Se non è presente alcun proxy, è comunque possibile usare ProxyCfg.exe per specificare un elenco di host che si considera attendibili per eseguire l'autenticazione NTLM. Un nome proxy è obbligatorio quando ProxyCfg.exe a questo scopo, ma è possibile usare qualsiasi stringa valida al posto di un nome proxy reale.

Per altre informazioni sui criteri di accesso automatico, vedere [Criteri di accesso automatico.](authentication-in-winhttp.md)

 

 
