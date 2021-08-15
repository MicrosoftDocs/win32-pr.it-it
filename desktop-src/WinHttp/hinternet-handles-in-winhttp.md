---
description: Microsoft Windows servizi HTTP (WinHTTP) usa gli handle per tenere traccia delle impostazioni e delle informazioni necessarie quando si usa il protocollo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Handle HINTERNET in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a76f925d11646ed2fe5b5d3732fe8972d979cdc6383a4d47e955c0e60a1390e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563272"
---
# <a name="hinternet-handles-in-winhttp"></a>Handle HINTERNET in WinHTTP

Microsoft Windows servizi HTTP (WinHTTP) usa gli handle per tenere traccia delle impostazioni e delle informazioni necessarie quando si usa il protocollo HTTP. Ogni handle mantiene le informazioni pertinenti a una sessione HTTP, a una connessione con un server HTTP o a una risorsa specifica. Questo argomento descrive i vari tipi di handle, le convenzioni di denominazione per questi handle e la relativa struttura gerarchica.

-   [Informazioni sugli handle HINTERNET](#about-hinternet-handles)
-   [Handle di denominazione](#naming-handles)
-   [Gestire la gerarchia](#handle-hierarchy)
-   [Spiegazione della gerarchia degli handle](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Informazioni sugli handle HINTERNET

Gli handle creati e usati da WinHTTP sono denominati **handle HINTERNET.** Le funzioni WinHTTP restituiscono **handle HINTERNET** non intercambiabili con altri handle, quindi non possono essere usate con funzioni come [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**o CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Analogamente, non è possibile usare altri handle con le funzioni WinHTTP. Ad esempio, un handle restituito da [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) non può essere passato [**a WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) Questi **handle HINTERNET** non possono essere chiusi mentre è in corso una chiamata API che usa l'handle. Per evitare un race condition, le applicazioni devono proteggere l'handle e impedirne la chiusura fino a quando la chiamata API è in corso.

Le funzioni Microsoft Win32 Internet (WinInet) usano anche handle **HINTERNET.** Tuttavia, gli handle usati nelle funzioni WinInet non possono essere intercambiati con gli handle usati nelle funzioni WinHTTP. Per altre informazioni su WinInet, vedere [Informazioni su WinINet.](/windows/desktop/WinInet/about-wininet)

La [**funzione WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) chiude gli handle **HINTERNET** WinHTTP.

## <a name="naming-handles"></a>Handle di denominazione

Nella documentazione di WinHTTP, le descrizioni delle funzioni nell'API (Application Programming Interface) e nel codice di esempio mostrano la creazione e l'uso di vari tipi di **handle HINTERNET.** Per tenere traccia dei diversi tipi di handle disponibili, la denominazione di questi handle è coerente. Nella tabella seguente vengono illustrati gli identificatori usati dalla convenzione nella documentazione.



| Tipo di handle       | Handle di creazione della funzione                                                                                                          | Identificatore |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Handle generico    | [**WinHttpOpen,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)o [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Handle di sessione    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Handle di connessione | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Handle di richiesta    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Gestire la gerarchia

Gli **handle HINTERNET** vengono gestiti in una gerarchia. L'handle restituito [**da WinHttpOpen è**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) l'handle **HINTERNET della** sessione. La **chiamata a WinHttpOpen** inizializza le funzioni WinHTTP e avvia un contesto di sessione che mantiene le informazioni utente e le impostazioni per tutta la durata dell'handle di sessione. [**WinHttpConnect specifica**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) un server HTTP o HTTPS di destinazione e crea un handle **HINTERNET di** connessione. Per impostazione predefinita, l'handle di connessione eredita le impostazioni per l'handle di sessione. A ogni risorsa specificata con una chiamata a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) viene assegnato un handle **HINTERNET di** richiesta.

Il diagramma seguente illustra la gerarchia degli **handle HINTERNET.** Ogni casella nel diagramma rappresenta una funzione WinHTTP che restituisce un **handle HINTERNET.**

![funzioni che creano handle](images/art-winhttp2.png)

Dopo la chiusura di un handle, l'applicazione deve essere preparata a ricevere notifiche di callback sull'handle fino a quando non viene restituito il valore **FINALE WINHTTP \_ CALLBACK STATUS \_ HANDLE \_ \_ CLOSED** per indicare che l'handle è completamente chiuso.

Un handle di sessione è l'elemento padre di qualsiasi handle di connessione usato per creare. Analogamente, sia l'handle di connessione che l'handle di sessione padre sono noti come elementi padre di qualsiasi handle di richiesta usato per creare l'handle di connessione.

Quando un handle padre viene chiuso, tutti gli elementi figlio che ha vengono invalidati indirettamente anche se non chiusi e le richieste successive che li usano hanno esito negativo con l'errore **ERROR \_ INVALID \_ HANDLE**. Non è possibile basarsi su richieste asincrone in sospeso per il corretto completamento.

Il diagramma seguente illustra le funzioni che usano l'handle **HINTERNET** creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Le caselle ombreggiate rappresentano le funzioni WinHTTP che creano gli handle e le caselle semplici mostrano le funzioni che usano tali **handle HINTERNET.** Il diagramma è anche organizzato per mostrare l'ordine in cui le funzioni WinHTTP vengono chiamate normalmente.

![funzioni che creano handle](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Spiegazione della gerarchia degli handle

In primo luogo, viene creato un handle di sessione [**con WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect richiede**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) l'handle di sessione come primo parametro e restituisce un handle di connessione per un server specificato. Un handle di richiesta viene creato [**da WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), che usa l'handle di connessione creato da [**WinHttpConnect.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) Se l'applicazione sceglie di aggiungere altre intestazioni alla richiesta o se è necessario che l'applicazione imposta le credenziali per l'autenticazione, è possibile chiamare [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) e [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) usando questo handle di richiesta. La richiesta viene inviata da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), che usa l'handle della richiesta. Dopo aver inviato la richiesta, è possibile inviare dati aggiuntivi al server usando [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)oppure l'applicazione può passare direttamente a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) per specificare che non vengono inviate altre informazioni al server. A questo punto, a seconda dello scopo dell'applicazione, l'handle della richiesta può essere usato per chiamare [**WinHttpQueryHeaders,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)o recuperare una risorsa [**con WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) [**e WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
