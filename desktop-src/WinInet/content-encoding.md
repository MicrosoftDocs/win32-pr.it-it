---
title: Codifica contenuto
description: A partire da Windows Server 2008 e Windows Vista, l'applicazione può indirizzare WinINet all'esecuzione della decodifica del contenuto per gli schemi di codifica del contenuto gzip e deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codifica contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1a91120e4ea01c4636c8d9942e968a0d69aeed50b6a037b31aa0241f3e933c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132884"
---
# <a name="content-encoding"></a>Codifica contenuto

Come specificato nel protocollo HTTP (RFC 2616), le applicazioni possono richiedere che il server restituirà risposte HTTP in formato codificato. Prima di Windows Server 2008 e Windows Vista, le richieste con codifica del contenuto venivano inviate all'applicazione per l'elaborazione al loro livello. A partire da Windows Server 2008 e Windows Vista, l'applicazione può indirizzare WinINet all'esecuzione della decodifica del contenuto per gli schemi di codifica del contenuto gzip e deflate.

Per abilitare la decodifica del contenuto, l'applicazione imposta l'opzione di decodifica che richiede a WinINet di eseguire la decodifica per loro conto. Tuttavia, l'abilitazione della decodifica non garantisce che WinINet eseguirà la decodifica del contenuto e l'applicazione deve essere preparata per gestire la decodifica. WinINet rimuove l'intestazione content-encoding dalla risposta quando la decodifica del contenuto viene eseguita correttamente. Le applicazioni devono gestire la decodifica del contenuto indipendentemente dal fatto che l'opzione di decodifica sia abilitata o disabilitata quando l'intestazione content-encoding è presente nella risposta.

Quando la decodifica è abilitata, l'applicazione deve specificare l'elenco delle codifiche supportate nellAccept-Encoding in intestazione della richiesta. LAccept-Encoding in header, tuttavia, non obbliga il server a inviare una risposta codificata. WinINet invierà all'applicazione risposte che non corrispondono all'elenco di codifiche accettabili.

L'elenco seguente descrive le condizioni in base alle quali WinINet eseguirà la decodifica del contenuto quando l'opzione è abilitata:

-   LAccept-Encoding deve essere presente nella richiesta e deve specificare gli schemi di codifica gzip, deflate o entrambi gli schemi di codifica gzip e deflate.
-   Lo schema di codifica specificato nell'intestazione Content-Encoding deve corrispondere a uno degli schemi di codifica specificati nell'intestazione Accept-Encoding codifica.
-   L'intestazione Content-Encoding nella risposta specifica un solo schema di codifica.
-   La risposta deve contenere una sola intestazione Content- Encoding. WinINet decodifica il contenuto codificato con un solo schema di codifica.
-   LCache-Control in header non deve contenere la direttiva no-transform.
-   L'intestazione Content-Range non deve essere presente nella risposta.

## <a name="setting-the-decompression-option"></a>Impostazione dell'opzione di decompressione

L'opzione di decodifica può essere impostata sull'handle di sessione, sull'handle di richiesta o sull'handle di connessione. L'handle su cui è impostata l'opzione di decodifica definisce l'ambito dell'opzione di decodifica. Ad esempio, l'impostazione della decodifica nella sessione consentirà di decodificare tutte le connessioni e le richieste create con tale handle.

Per impostare l'opzione di decodifica, l'applicazione chiama [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con l'handle restituito da [**InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) **L'opzione INTERNET OPTION HTTP \_ \_ \_ DECODING** è specificata nel *parametro dwOption* e il parametro *lpBuffer* punta a una variabile booleana impostata su true. Per disabilitare la decodifica, l'applicazione chiama **InternetSetOption** con l'opzione **INTERNET OPTION HTTP \_ \_ \_ DECODING** e la variabile booleana impostata su false.

Quando l'opzione di decodifica è impostata, WinINet esegue la decodifica nella richiesta quando l'applicazione [**chiama InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) Se WinINet rileva un errore durante l'esecuzione della decodifica del contenuto, la chiamata a **InternetReadFile** ha esito negativo con **errore INTERNET \_ \_ DECODING \_ FAILED**. Quando la decodifica non riesce, l'applicazione ha due opzioni: può rimuovere l'intestazione Accept-Encoding e inviare di nuovo la richiesta oppure impostare l'opzione **INTERNET \_ OPTION HTTP \_ \_ DECODING** nella richiesta su false e quindi inviare nuovamente la richiesta. Se l'opzione di decodifica è impostata su false, l'applicazione deve controllare l'intestazione Content-Encoding ed eseguire qualsiasi decodifica a livello di applicazione.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 