---
description: In questo argomento vengono descritte le differenze più importanti tra la versione 5,1 e la versione 5,0 di WinHTTP.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Novità di WinHTTP 5,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909d5ae8fb1d169af01782d21d2ead56b25c940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307109"
---
# <a name="whats-new-in-winhttp-51"></a>Novità di WinHTTP 5,1

In questo argomento vengono descritte le differenze più importanti tra la versione 5,1 e la versione 5,0 di WinHTTP. Molte di queste differenze richiedono modifiche al codice nelle applicazioni che eseguono la migrazione dalla versione 5,0 alla versione 5,1. Alcune delle funzionalità della versione 5,1 sono disponibili solo a partire da Windows Server 2003 e Windows XP con Service Pack 2 (SP2), in particolare le funzionalità relative al miglioramento della sicurezza del client da server Web dannosi.

> [!IMPORTANT]
> Con il rilascio di WinHTTP versione 5,1, il download di WinHTTP 5,0 non è più disponibile. A partire dal 1 ° ottobre 2004, Microsoft ha rimosso il download di WinHTTP 5,0 SDK da MSDN e ha terminato il supporto tecnico per la versione 5,0.

 

## <a name="dll-name-change"></a>Modifica nome DLL

Il nome della nuova DLL WinHTTP 5,1 è Winhttp.dll, mentre il nome della DLL WinHTTP 5,0 è Winhttp5.dll.

WinHTTP 5,0 e 5,1 possono coesistere nello stesso sistema; WinHTTP 5,1 non sostituisce o esegue l'installazione in WinHTTP 5,0.

## <a name="redistribution"></a>Ridistribuzione

WinHTTP 5,1 è disponibile solo con Windows Server 2003, Windows 2000 Professional con Service Pack 3 (SP3), Windows XP con Service Pack 1 (SP1) e sistemi operativi successivi. Un file di modulo unione ridistribuibile (MSM) non è disponibile per WinHTTP 5,1.

## <a name="winhttprequest-progid"></a>ProgID WinHttpRequest

Il ProgID del componente WinHttpRequest è stato modificato da "WinHttp. WinHttpRequest. 5" a "WinHttp. WinHttpRequest. 5.1". È stato modificato anche il CLSID della classe [**WinHttpRequest**](winhttprequest.md) .

## <a name="async-callback-behavior-change"></a>Modifica del comportamento di callback asincrono

Quando si chiamano le funzioni [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) e [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) in modalità asincrona, non basarsi sui rispettivi parametri *lpdwNumberOfBytesWritten*, *lpdwNumberOfBytesAvailable* e *lpdwNumberOfBytesRead* out da impostare. Se la chiamata di funzione viene completata in modo asincrono, WinHTTP non scrive in questi puntatori forniti dal codice dell'applicazione. Al contrario, l'applicazione deve recuperare questi valori usando i parametri *lpvStatusInformation* e *dwStatusInformationLength* per la funzione di callback.

## <a name="changes-to-default-settings"></a>Modifiche alle impostazioni predefinite

Le modifiche alle impostazioni predefinite includono:

-   La verifica del certificato del server SSL è abilitata per impostazione predefinita in WinHTTP 5,1. WinHTTP 5,0 non gestisce gli errori riscontrati durante la convalida del certificato del server come errori irreversibili; vengono segnalati all'applicazione tramite una notifica di callback di **\_ errore protetto** , ma non provoca l'interruzione della richiesta. WinHTTP 5,1, in alternativa, gestisce gli errori di convalida del certificato server come errori irreversibili che interrompono la richiesta. L'applicazione può indicare a WinHTTP di ignorare un piccolo subset di errori del certificato, ad esempio una CA sconosciuta, una data del certificato non valida o scaduta o un nome soggetto del certificato non valido, usando l'opzione per i **\_ flag di \_ sicurezza \_ dell'opzione WinHTTP** .
-   Il supporto per l'autenticazione Passport è disabilitato per impostazione predefinita in WinHTTP 5,1. È possibile abilitare il supporto Passport con l'opzione **WinHTTP \_ \_ Configure \_ Passport \_ AUTH** . Anche la ricerca automatica delle credenziali Passport nel portachiavi è disabilitata per impostazione predefinita.
-   Modifica del comportamento di reindirizzamento: i reindirizzamenti HTTP da un **HTTPS sicuro:** URL a un normale **http:** URL non sono più seguiti automaticamente per impostazione predefinita per motivi di sicurezza. È disponibile una nuova opzione, **i \_ \_ \_ criteri di reindirizzamento delle opzioni WinHTTP**, per eseguire l'override del comportamento di reindirizzamento predefinito in WinHTTP 5,1. Con il componente COM **WinHttpRequest** , usare la nuova **opzione \_ EnableHttpsToHttpRedirects di WinHttpRequestOption** per abilitare i reindirizzamenti da https: a http: URL.
-   Quando viene creato un file di traccia WinHTTP, l'accesso è limitato a un ACL in modo che solo gli amministratori possano leggere o scrivere il file. L'account utente con cui è stato creato il TraceFile può anche modificare l'ACL per concedere ad altri utenti l'accesso. Questa protezione è disponibile solo nei file System che supportano la protezione. ovvero NTFS, non FAT32.
-   A partire da Windows Server 2003 e Windows XP con SP2, l'invio di richieste alle seguenti porte note e non HTTP è limitato per motivi di sicurezza: 21 (FTP), 25 (SMTP), 70 (GOPHER), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   A partire da Windows Server 2003 e Windows XP con SP2, la quantità massima di dati di intestazione che WinHTTP accetta in una risposta HTTP è 64K, per impostazione predefinita. Se la risposta HTTP del server contiene più 64K di dati di intestazione totali, WinHTTP non riesce a usare la richiesta con errore WinHTTP: errore di **\_ \_ \_ \_ risposta del server non valido** . È possibile eseguire l'override di questo limite di 64K utilizzando l'opzione per le **\_ \_ \_ \_ \_ dimensioni massime dell'intestazione della risposta** per il nuovo WinHTTP.

## <a name="ipv6-support"></a>Supporto IPv6

WinHTTP 5,1 aggiunge il supporto per protocollo Internet versione 6 (IPv6). WinHTTP può inviare richieste HTTP a un server il cui nome DNS viene risolto in un indirizzo IPv6 e a partire da Windows Server 2003 e Windows XP con SP2, WinHTTP supporta anche indirizzi letterali IPv6.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Nuove opzioni nell'API C/C++ per WinHTTP

WinHTTP 5,1 implementa le nuove opzioni seguenti:

<dl> " \# Definisci l' \_ opzione \_ per il Passport di \_ disconnessione \_ 86"  
" \# define \_ \_ \_ URL Passport return \_ URL 87"  
" \# definire i \_ criteri di reindirizzamento delle opzioni WinHTTP \_ \_ 88"  
</dl>

A partire da Windows Server 2003 e Windows XP con SP2, WinHTTP 5,1 implementa le nuove opzioni seguenti. In Windows 2000 Professional con SP3 o Windows XP con SP1, tuttavia, le chiamate a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) o [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con questi ID opzione hanno esito negativo:

<dl> " \# definire il \_ timeout di risposta di ricezione dell'opzione WinHTTP \_ \_ \_ 7"  
" \# Definisci l' \_ opzione WinHTTP \_ Max \_ http \_ \_ reindirizzamenti automatici 89"  
" \# definizione \_ opzione WinHTTP \_ Max \_ http \_ status \_ continua 90"  
" \# definizione delle \_ dimensioni massime dell'intestazione della risposta per l'opzione WinHTTP \_ \_ \_ \_ 91"  
" \# definire le \_ dimensioni massime di svuotamento della risposta per l'opzione WinHTTP \_ \_ \_ \_ 92"  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Nuove opzioni nel componente WinHttpRequest 5,1

Il componente WinHttpRequest 5,1 implementa le nuove opzioni seguenti:

<dl> "WinHttpRequestOption \_ RevertImpersonationOverSsl"  
"WinHttpRequestOption \_ EnableHttpsToHttpRedirects"  
"WinHttpRequestOption \_ EnablePassportAuthentication"  
</dl>

Le seguenti nuove opzioni di WinHttpRequest 5,1 sono disponibili a partire da Windows Server 2003 e Windows XP con SP2:

<dl> "WinHttpRequestOption \_ MaxAutomaticRedirects"  
"WinHttpRequestOption \_ MaxResponseHeaderSize"  
"WinHttpRequestOption \_ MaxResponseDrainSize"  
"WinHttpRequestOptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>I proxy non sono attendibili quando la sicurezza dell'accesso automatico è impostata su High

In WinHTTP 5,0, i server proxy sono sempre attendibili per l'accesso automatico. Questa opzione non è più valida per WinHTTP 5,1 in esecuzione in Windows Server 2003 e Windows XP con SP2 quando è impostata l'opzione per i criteri **elevati del livello di sicurezza di WinHTTP \_ Autologon \_ \_ \_** .

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API Web Proxy Auto-Discovery (AutoProxy)

Per semplificare la configurazione delle impostazioni proxy per le applicazioni basate su WinHTTP, WinHTTP implementa ora il protocollo WPAD (Web Proxy Auto-Discovery), noto anche come *AutoProxy*. Si tratta dello stesso protocollo che i Web browser, ad esempio Internet Explorer, implementano per individuare automaticamente la configurazione del proxy senza richiedere a un utente finale di specificare manualmente un server proxy. Per supportare AutoProxy, WinHTTP 5,1 implementa una nuova funzione C/C++, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), più due funzioni di supporto, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Problemi noti

I problemi seguenti sono noti in WinHTTP 5,1 su Windows 2000 Professional con SP3 e Windows XP con SP1. Questi problemi vengono risolti per WinHTTP a partire da Windows Server 2003 e Windows XP con SP2:

-   Se l'applicazione usa la funzione [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) o il metodo [**setimeouts**](iwinhttprequest-settimeouts.md) sul componente [**WinHttpRequest**](iwinhttprequest-interface.md) per impostare un timeout di risoluzione DNS non infinito, ad esempio il parametro *dwResolveTimeout* , si verifica una perdita di handle del thread ogni volta che WinHTTP risolve un nome DNS. Per un numero elevato di richieste HTTP, ciò causa una perdita di memoria significativa. La soluzione alternativa consiste nel lasciare invariata l'impostazione predefinita di timeout di risoluzione infinita (il valore 0 indica un timeout infinito). Questa operazione è consigliata in ogni caso perché i timeout di supporto per le risoluzioni dei nomi DNS in WinHTTP sono costosi in termini di prestazioni. Per Windows 2000 e versioni successive, l'impostazione di un timeout di risoluzione DNS in WinHTTP non è necessaria perché il servizio client DNS sottostante implementa il proprio timeout di risoluzione.
-   Quando si elaborano richieste asincrone, WinHTTP non gestisce correttamente la rappresentazione del thread. In questo modo le richieste che richiedono l'autenticazione NTLM/Negotiate avranno esito negativo, a meno che le credenziali non vengano specificate in modo esplicito mediante le funzioni [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) .

 

 



