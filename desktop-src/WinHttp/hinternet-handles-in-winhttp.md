---
description: I servizi HTTP di Microsoft Windows (WinHTTP) utilizzano gli handle per tenere traccia delle impostazioni e delle informazioni necessarie quando si utilizza il protocollo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Handle HINTERNET in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551704"
---
# <a name="hinternet-handles-in-winhttp"></a>Handle HINTERNET in WinHTTP

I servizi HTTP di Microsoft Windows (WinHTTP) utilizzano gli handle per tenere traccia delle impostazioni e delle informazioni necessarie quando si utilizza il protocollo HTTP. Ogni handle mantiene le informazioni pertinenti a una sessione HTTP, una connessione a un server HTTP o una risorsa specifica. In questo argomento vengono descritti i vari tipi di handle, le convenzioni di denominazione per questi handle e la relativa struttura gerarchica.

-   [Informazioni sugli handle HINTERNET](#about-hinternet-handles)
-   [Nomi degli handle](#naming-handles)
-   [Gestisci gerarchia](#handle-hierarchy)
-   [Spiegazione della gerarchia di handle](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Informazioni sugli handle HINTERNET

Gli handle creati e usati da WinHTTP sono detti handle **HINTERNET** . Le funzioni WinHTTP restituiscono handle **HINTERNET** che non sono intercambiabili con altri handle, quindi non possono essere usate con funzioni come [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Analogamente, non è possibile usare altri handle con funzioni WinHTTP. Un handle restituito da [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , ad esempio, non può essere passato a [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Non è possibile chiudere questi handle **HINTERNET** mentre è in corso una chiamata API che usa l'handle. Per evitare un race condition, le applicazioni devono proteggere l'handle e impedirne la chiusura fino a quando è in corso la chiamata all'API.

Anche le funzioni Microsoft Win32 Internet (WinInet) utilizzano handle **HINTERNET** . Tuttavia, gli handle utilizzati nelle funzioni WinInet non possono essere scambiati con gli handle utilizzati nelle funzioni WinHTTP. Per ulteriori informazioni su WinInet, vedere [informazioni su WinInet](/windows/desktop/WinInet/about-wininet).

La funzione [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) chiude gli handle **HINTERNET** di WinHTTP.

## <a name="naming-handles"></a>Nomi degli handle

Nella documentazione di WinHTTP, le descrizioni delle funzioni nel Application Programming Interface (API) e nel codice di esempio illustrano la creazione e l'uso di diversi tipi di handle **HINTERNET** . Per tenere traccia dei diversi tipi di handle disponibili, la denominazione di questi handle è coerente. Nella tabella seguente vengono illustrati gli identificatori utilizzati dalla convenzione nella documentazione.



| Tipo di handle       | Handle creazione funzione                                                                                                          | Identificatore |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Handle generico    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)o [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Handle di sessione    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Handle di connessione | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Handle di richiesta    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Gestisci gerarchia

Gli handle **HINTERNET** vengono mantenuti in una gerarchia. L'handle restituito da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) è l'handle **HINTERNET** della sessione. La chiamata a **WinHttpOpen** Inizializza le funzioni WinHTTP e avvia un contesto di sessione che mantiene le informazioni e le impostazioni dell'utente per tutta la durata dell'handle di sessione. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) specifica un server http o HTTPS di destinazione e crea un handle **HINTERNET** di connessione. Per impostazione predefinita, l'handle di connessione eredita le impostazioni per l'handle di sessione. A ogni risorsa specificata con una chiamata a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) viene assegnato un handle **HINTERNET** della richiesta.

Nel diagramma seguente viene illustrata la gerarchia di handle **HINTERNET** . Ogni casella del diagramma rappresenta una funzione WinHTTP che restituisce un handle **HINTERNET** .

![funzioni che creano handle](images/art-winhttp2.png)

Dopo la chiusura di un handle, l'applicazione deve essere preparata a ricevere notifiche di callback sull'handle fino a quando non viene restituito il valore chiuso dell'handle di callback WinHTTP finale per indicare che l'handle è **\_ \_ stato \_ \_** completamente chiuso.

Un handle di sessione viene definito l'elemento padre di qualsiasi handle di connessione usato per creare; Analogamente, sia l'handle di connessione che il relativo handle della sessione padre sono elementi padre di qualsiasi handle di richiesta che l'handle di connessione viene utilizzato per creare.

Quando un handle padre viene chiuso, tutti gli elementi figlio in essa inclusi vengono invalidati indirettamente anche se non vengono chiusi e le successive richieste che li utilizzano hanno esito negativo e l'errore non è **\_ valido \_**. Non è possibile fare affidamento sulle richieste asincrone in sospeso per il corretto completamento.

Il diagramma seguente illustra le funzioni che usano l'handle **HINTERNET** creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Le caselle ombreggiate rappresentano le funzioni WinHTTP che creano handle e le caselle semplici mostrano le funzioni che utilizzano tali handle **HINTERNET** . Il diagramma è organizzato anche per indicare l'ordine in cui le funzioni WinHTTP sono normalmente chiamate.

![funzioni che creano handle](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Spiegazione della gerarchia di handle

Viene innanzitutto creato un handle di sessione con [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) richiede l'handle di sessione come primo parametro e restituisce un handle di connessione per un server specificato. Un handle di richiesta viene creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), che usa l'handle di connessione creato da [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect). Se l'applicazione sceglie di aggiungere ulteriori intestazioni alla richiesta o se è necessario che l'applicazione imposti le credenziali per l'autenticazione, è possibile chiamare [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) e [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) utilizzando questo handle di richiesta. La richiesta viene inviata da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), che usa l'handle della richiesta. Dopo l'invio della richiesta, i dati aggiuntivi possono essere inviati al server tramite [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)o l'applicazione può passare direttamente a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) per specificare che al server non vengono inviate altre informazioni. A questo punto, a seconda dello scopo dell'applicazione, l'handle della richiesta può essere usato per chiamare [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)o recuperare una risorsa con [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) e [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
