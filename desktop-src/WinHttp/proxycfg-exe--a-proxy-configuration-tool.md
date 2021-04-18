---
description: In questo argomento viene illustrato l'utilizzo dello strumento di configurazione proxy di Microsoft Windows HTTP Services (WinHTTP), &\# 0034; ProxyCfg.exe&\# 0034;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe e ProxyCfg.exe proxy Strumenti di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524828"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe e ProxyCfg.exe proxy Strumenti di configurazione

* * Windows Vista e Windows Server 2008: * *

ProxyCfg.exe è stato deprecato. Viene sostituito daNetsh.exe comandi [ WinHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) .

In questo argomento viene illustrato l'utilizzo dello strumento di configurazione proxy di [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , "ProxyCfg.exe".

Esistono due modi per accedere ai server HTTP e Secure Hypertext Transfer Protocol (HTTPS) tramite un proxy usando i servizi HTTP di Microsoft Windows (WinHTTP). In primo luogo, è possibile specificare le impostazioni del proxy all'interno dell'applicazione WinHTTP. In secondo luogo, è possibile specificare le impostazioni proxy predefinite dall'esterno dell'applicazione utilizzando l'utilità di configurazione proxy presente nella directory% windir% \\ system32.

È possibile impostare a livello di codice i dati del proxy all'interno dell'applicazione o dello script. Se si sta scrivendo un'applicazione utilizzando l'API WinHTTP, utilizzare una delle due tecniche seguenti per modificare le impostazioni del proxy.

-   Usare la funzione [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . Specificare il tipo di accesso nel secondo parametro, il nome del proxy nel terzo parametro e un elenco di bypass nel quarto parametro. Nell'esempio seguente viene illustrato come è possibile utilizzare la funzione [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) per impostare i dati del proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Usare la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) . Il flag del [**\_ \_ proxy dell'opzione WinHTTP**](option-flags.md) consente di specificare le impostazioni proxy con una struttura di [**\_ \_ informazioni proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) . Nell'esempio di codice seguente viene illustrato come utilizzare la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare i dati del proxy.

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

Se si scrive uno script o un'applicazione utilizzando l'oggetto [**WinHttpRequest**](winhttprequest.md) , utilizzare la tecnica seguente per modificare le impostazioni del proxy.

-   Usare il metodo [**seproxy**](iwinhttprequest-setproxy.md) . Specificare il tipo di accesso nel primo parametro, il nome del proxy nel secondo parametro e un elenco di bypass nel terzo parametro. Nell'esempio seguente viene illustrato come utilizzare il metodo [**seproxy**](iwinhttprequest-setproxy.md) nello script per impostare i dati del proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Per specificare le impostazioni predefinite ed eliminare la necessità di utilizzare il metodo [**seproxy**](iwinhttprequest-setproxy.md) o la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , utilizzare l'utilità di configurazione del proxy. Utilizzando questa utilità, è possibile specificare che l'applicazione acceda direttamente a una rete, tramite un proxy o tramite una combinazione di accesso diretto e proxy specificando un elenco di bypass. Quando si usa l'API WinHTTP, lo strumento di configurazione del proxy determina solo le impostazioni quando si passa il flag **predefinito del tipo di \_ accesso \_ \_ WinHTTP** all'API [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . Per impostazione predefinita, l'oggetto [**WinHttpRequest**](winhttprequest.md) utilizza le impostazioni dello strumento di configurazione del proxy.

Le impostazioni proxy per WinHTTP non sono le impostazioni proxy per Microsoft Internet Explorer. Non è possibile configurare le impostazioni proxy per WinHTTP nel pannello di controllo di Microsoft Windows. L'utilizzo dell'utilità di configurazione proxy WinHTTP non modifica le impostazioni utilizzate per Internet Explorer.

> [!Note]  
> Se si tenta di aprire e inviare una richiesta HTTP utilizzando WinHTTP e le impostazioni del proxy non sono corrette, si verificherà un errore.

 

## <a name="command-line-parameters"></a>Parametri della riga di comando

Nella tabella seguente sono elencati i parametri della riga di comando disponibili per l'utilizzo con lo strumento ProxyCfg.exe.



| Parametro | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno      | Quando non viene specificato alcun parametro, vengono visualizzate le impostazioni proxy WinHTTP correnti.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Vengono visualizzate le informazioni della guida.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Specifica che le applicazioni WinHTTP accedono direttamente alla rete, senza un proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Specifica il server proxy. È anche possibile specificare un elenco facoltativo di server a cui si accede senza un proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Specifica che le applicazioni WinHTTP utilizzano le impostazioni proxy dell'utente corrente per Internet Explorer. Questo parametro non funziona se Internet Explorer rileva automaticamente le impostazioni proxy oppure se usa un URL di configurazione automatico per impostare le informazioni sul proxy.                                                                                                                                                      |
| i         | Specifica che le applicazioni WinHTTP utilizzano le impostazioni proxy dell'utente corrente per Internet Explorer. Questa operazione funziona solo quando non è stato usato in precedenza ProxyCfg.exe. Se ProxyCfg.exe è installato, specificare che il parametro della riga di comando "u" utilizza le impostazioni manuali. Questo parametro non funziona se Internet Explorer rileva automaticamente le impostazioni proxy oppure se usa un URL di configurazione automatico per impostare le informazioni sul proxy. |



 

È possibile specificare proxy in una stringa delimitata da spazi. Gli elenchi proxy possono contenere il numero di porta utilizzato per accedere al proxy. Per elencare un proxy per un protocollo specifico, la stringa deve seguire il formato, <protocol> = https://<\_ nome proxy>. I protocolli validi sono HTTP e HTTPS. Ad esempio, per elencare un proxy HTTP, una stringa valida è http = https://http\_proxy\_name:80 , dove \_ il \_ nome del proxy HTTP è il nome del server proxy e 80 è il numero di porta che è necessario usare per accedere al proxy. Se il proxy usa il numero di porta predefinito per quel protocollo, è possibile omettere il numero di porta. Se un nome proxy è elencato da solo, è possibile utilizzarlo come proxy predefinito per tutti i protocolli che non dispongono di un proxy specificato. Ad esempio, http = https://http\_proxy altro \_ proxy usa \_ il proxy HTTP per qualsiasi operazione http, mentre il protocollo HTTPS usa il proxy denominato altro \_ proxy.

Nell'elenco proxy bypass è possibile elencare nomi host o indirizzi IP locali noti localmente. Questo elenco può contenere caratteri jolly, ad esempio " \* ", che fanno sì che l'applicazione ignori il server proxy per gli indirizzi che soddisfano il criterio specificato, ad esempio " \* . Microsoft.com" o " \* . org". I caratteri jolly devono essere i caratteri più a sinistra nell'elenco. Ad esempio \* , "AAA". non è supportato. Per elencare più indirizzi e nomi host, separarli con spazi vuoti o punti e virgola nella stringa di bypass del proxy. Se si specifica la <local> macro, la funzione ignora qualsiasi nome host che non contiene un punto.

> [!WARNING]
> Dopo l'esecuzione di Proxycfg.exe, non è possibile ripristinare le impostazioni proxy precedenti. Tuttavia, è possibile rimuovere completamente le impostazioni del proxy.

 

## <a name="usage"></a>Utilizzo

Per utilizzare lo strumento di configurazione del proxy, aprire una finestra del prompt dei comandi ed eseguire l'utilità di configurazione del proxy con i parametri della riga di comando appropriati. Nella sezione seguente vengono forniti esempi di sintassi.

## <a name="example-syntax"></a>Sintassi di esempio

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Esempio 1: usare un proxy solo per le risorse esterne

Di seguito è riportato l'utilizzo più comune per Proxycfg.exe. Questo comando specifica che è possibile accedere ai server HTTP e HTTPS tramite il server proxy denominato " \_ server proxy", ad eccezione dei nomi host che non contengono un punto.

**server proxy proxycfg-p \_ " <local> "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Esempio 2: usare un proxy per tutte le risorse

Nell'esempio seguente viene specificato che è possibile accedere ai server HTTP e HTTPS tramite il server proxy denominato " \_ server proxy". Non è specificato alcun elenco di bypass.

**server proxy proxycfg-p \_**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Esempio 3: usare un proxy diverso per le risorse protette

Nell'esempio seguente viene specificato che è possibile accedere ai server HTTP tramite il proxy \_ proxy http ed è possibile accedere ai server HTTPS tramite il \_ proxy HTTPS. Il proxy viene ignorato dai siti Intranet locali e da qualsiasi sito nel \* dominio. Microsoft.com.

**proxycfg-p "http = \_ proxy HTTP HTTPS = \_ proxy HTTPS" " <local> ; \* . microsoft.com "**

## <a name="removing-proxycfgexe"></a>Rimozione di ProxyCfg.exe

Dopo aver utilizzato lo strumento di configurazione del proxy, non è possibile ripristinare le impostazioni proxy originali. Tuttavia, se necessario, è possibile rimuovere le impostazioni del registro di sistema create dall'utilità. Per rimuovere le voci del registro di sistema create da ProxyCfg.exe, è necessario eliminare il valore **WinHttpSettings** dalla seguente chiave del registro di sistema.

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings** \\ **Connections** \\ **WinHttpSettings**

Se si elimina il valore *WinHttpSettings* , verranno rimosse tutte le configurazioni del proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe e autenticazione

L'utilità di configurazione del proxy imposta i criteri di autenticazione predefiniti. Poiché non è consigliabile eseguire l'autenticazione NTLM con host non attendibili, per impostazione predefinita l'autenticazione NTLM si verifica solo automaticamente con gli host nell'elenco proxy bypass. Se non è presente alcun proxy, è comunque possibile utilizzare ProxyCfg.exe per specificare un elenco di host da ignorare che si considera attendibile per eseguire l'autenticazione NTLM. Un nome proxy è obbligatorio quando si usa ProxyCfg.exe a questo scopo, ma è possibile usare qualsiasi stringa valida al posto di un nome di proxy reale.

Per ulteriori informazioni sui criteri di accesso automatico, vedere [criteri di accesso automatico](authentication-in-winhttp.md).

 

 
