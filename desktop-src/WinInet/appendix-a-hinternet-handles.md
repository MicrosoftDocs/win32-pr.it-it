---
title: Handle HINTERNET
description: Questa sezione contiene informazioni sugli handle usati dalle funzioni WinINet e sulla gerarchia in cui funzionano.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051932"
---
# <a name="hinternet-handles"></a>Handle HINTERNET

Questa sezione contiene informazioni sugli handle usati dalle funzioni WinINet e sulla gerarchia in cui funzionano.

-   [Informazioni sugli handle HINTERNET](#about-hinternet-handles)
-   [Gestire la gerarchia](#handle-hierarchy)
-   [Gerarchia FTP](#ftp-hierarchy)
-   [Gerarchia HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Informazioni sugli handle HINTERNET

Gli handle creati e usati dalle funzioni WinINet sono di tipo **HINTERNET.** Le funzioni WinINet restituiscono **handle HINTERNET** non intercambiabili con altri tipi di handle. Pertanto, non possono essere usati con funzioni come [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Analogamente, non è possibile usare altri tipi di handle con le funzioni WinINet. Ad esempio, un handle restituito [**da CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) non può essere passato a [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)

La [**funzione InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) chiude handle di tipo **HINTERNET.** Si noti che i valori di handle vengono riciclati rapidamente. Pertanto, se un handle viene chiuso e viene generato immediatamente un nuovo handle, è probabile che il nuovo handle abbia lo stesso valore dell'handle appena chiuso.

## <a name="handle-hierarchy"></a>Gestire la gerarchia

Gli **handle HINTERNET** vengono mantenuti in una gerarchia ad albero. L'handle restituito [**dalla funzione InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) è il nodo radice. Gli handle restituiti dalla [**funzione InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) occupano il livello successivo. Gli handle restituiti [**dalle funzioni FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) sono i nodi foglia.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Anche gli handle restituiti da , [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)e [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) sono nodi foglia.

Nel diagramma seguente viene illustrata la gerarchia degli **handle HINTERNET.** Ogni casella nel diagramma rappresenta una funzione che restituisce un **handle HINTERNET.**

![Funzioni che creano handle](images/ax-wnt01.png)

Al livello superiore è disponibile la [**funzione InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) che crea l'handle radice. Il livello successivo contiene le [**funzioni InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**e InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Le funzioni che usano l'handle restituito [**da InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) costituiscono l'ultimo livello.

Il diagramma seguente illustra le funzioni che dipendono dall'handle creato da [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Le caselle ombreggiate rappresentano le funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione associata.

![Funzioni che usano l'handle internetopenurl](images/ax-wnt02.png)

Le [**funzioni InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) usano l'handle **HINTERNET** creato [**da InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

## <a name="ftp-hierarchy"></a>Gerarchia FTP

Il diagramma seguente illustra le funzioni FTP che dipendono dall'handle di sessione FTP restituito da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![Funzioni che usano l'handle di sessione FTP](images/ax-wnt06.png)

Le [**funzioni FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) usano tutte l'handle **HINTERNET** creato da [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

Nel diagramma seguente vengono illustrate le due funzioni FTP che restituiscono handle e le funzioni che dipendono da essi. Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![Funzioni che usano l'handle da ftpopen e ftpfindfirstfile](images/ax-wnt03.png)

La [**funzione InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) dipende dall'handle creato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), mentre [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) usano l'handle creato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Gerarchia HTTP

Il diagramma seguente illustra le relazioni delle funzioni usate per il protocollo HTTP. Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![Funzioni che usano l'handle da httpopenrequest](images/ax-wnt05.png)

Le [**funzioni HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) [**e InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) dipendono dall'handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

Il diagramma seguente illustra le funzioni che usano l'handle **HINTERNET** creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) dopo che è stato inviato da [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET,** mentre le caselle semplici rappresentano le funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.

![Funzioni che usano l'handle dopo httpsendrequest](images/ax-wnt07.png)

Dopo [**che HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) ha usato l'handle restituito da [**HttpOpenRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)può essere usato da [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer.**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)

![Funzioni che usano l'handle dopo httpsendrequestex](images/ax-wnt08.png)

Dopo [**che HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) ha usato l'handle restituito da [**HttpOpenRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)l'handle può essere usato da [**HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)e [**InternetWriteFile.**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) Dopo [**la chiamata a HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) l'handle può essere usato da [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)e [**InternetQueryDataAvailable.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 