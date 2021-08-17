---
title: Operazione asincrona
description: In modalità asincrona, un'applicazione può eseguire qualsiasi funzione che include un valore di contesto come uno dei relativi parametri e può continuare a eseguire altri comandi o funzioni mentre l'applicazione attende che la funzione completi l'attività.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e494b79b28b9aaf005fc6b1790d0cf84b07ceade6606f03ce03198426ac33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562093"
---
# <a name="asynchronous-operation"></a>Operazione asincrona

Il tempo necessario a un'applicazione per accedere a una risorsa Internet dipende da diversi fattori, ad esempio la connessione usata, il server in cui si trova la risorsa e il numero di utenti che tentano di accedere alla risorsa. Per le applicazioni che scaricano più risorse o gestiscono più attività (inclusi uno o più download), attendere il completamento di ogni download prima di passare all'attività successiva può essere estremamente inefficiente. Per ridurre il tempo di attesa di un'applicazione, molte delle funzioni WinINet possono funzionare in modo asincrono.

In modalità asincrona, un'applicazione può eseguire qualsiasi funzione che include un valore di contesto come uno dei relativi parametri e può continuare a eseguire altri comandi o funzioni mentre l'applicazione attende che la funzione completi l'attività. Durante il completamento dell'attività, una funzione di callback dello stato fornita dall'applicazione viene notificata lo stato dell'attività e il momento in cui è stata completata. In questo momento, la funzione di callback dello stato può chiamare altre funzioni o eseguire qualsiasi altra attività richiesta dipendente dal completamento dell'attività.

Non esiste alcuna afinità del thread di callback quando si chiama WinINet in modo asincrono: una chiamata può essere avviata da un thread, ma qualsiasi altro thread può ricevere il callback.

-   [Vantaggi](#benefits)
-   [Scenari](#scenarios)
-   [Argomenti correlati](#related-topics)

## <a name="benefits"></a>Vantaggi

Il funzionamento asincrono offre diversi vantaggi. Esempio:

-   Download simultaneo di più risorse Internet.

    È possibile connettersi a più risorse Internet contemporaneamente e scaricarle non appena diventano disponibili.

-   Aumento delle prestazioni dell'applicazione.

    Un'applicazione che usa le funzioni WinINet in modo asincrono non deve attendere il completamento della richiesta, quindi l'applicazione è libera di eseguire altre attività che non dipendono dalla richiesta, migliorando così le prestazioni complessive dell'applicazione.

-   Monitorare lo stato del download.

    La funzione di callback dello stato riceve notifiche durante l'elaborazione di una richiesta. Se necessario, l'applicazione può usare le informazioni fornite da tale funzione di callback dello stato per mantenere l'utente informato sullo stato dell'operazione o per interrompere le richieste che stanno richiedendo troppo tempo per il completamento.

## <a name="scenarios"></a>Scenari

Si supponiamo che l'applicazione deve scaricare i prezzi del caffè dai siti Downfall Coffee & Tea e Fourth Coffee e confrontare i prezzi. Il sito Fourth Coffee ha in genere un tempo di risposta più lento, quindi l'applicazione deve scaricare prima le informazioni da Downfall Coffee & Tea.

Vengono sviluppate due versioni dell'applicazione. Uno funziona in modo sincrono, scaricando prima i prezzi dal sito Downfall Coffee & Tea e quindi i prezzi dal sito Fourth Coffee. Il secondo funziona in modo asincrono, inviando richieste a entrambi i siti e scaricando i prezzi quando diventano disponibili.

La tabella seguente illustra cosa accadrebbe se il sito Fourth Coffee fosse più veloce in un determinato giorno.



| Evento                                                            | Versione sincrona                        | Versione asincrona                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Avvio                                                            | Inviare una richiesta a Downfall Coffee & Tea      | Inviare richieste a Downfall Coffee & Tea e Fourth Coffee |
| Richiesta dalla versione asincrona a Fourth Coffee completata | Attesa                                    | Scaricare i prezzi da Fourth Coffee                       |
| Richiesta di downfall coffee & Tea completata                       | Scaricare i prezzi da Downfall Coffee & Tea | Scaricare i prezzi da Downfall Coffee & Tea               |
| Dopo il download dei prezzi di & coffee & Tea              | Inviare la richiesta a Fourth Coffee              | Confrontare i prezzi                                           |
| Confronto della versione asincrona completato                      | Attesa                                    | Operazione completata                                       |
| Richiesta dalla versione sincrona a Fourth Coffee completata  | Scaricare i prezzi da Fourth Coffee         | n/d                                                      |
| Dopo il download dei prezzi di Fourth Coffee                      | Confrontare i prezzi                             | n/d                                                      |
| Confronto della versione sincrona completato                       | Operazione completata                         | n/d                                                      |



 

Un altro esempio potrebbe essere un Web browser, ad esempio Microsoft Internet Explorer. Quando il browser scarica una pagina, spesso deve scaricare altre risorse, ad esempio immagini e file audio. In modalità asincrona, la pagina e le risorse associate possono essere richieste contemporaneamente e scaricate non appena diventano disponibili, invece di richiedere e scaricare la pagina e ogni risorsa una alla volta.

## <a name="related-topics"></a>Argomenti correlati

Di seguito sono riportati collegamenti correlati.

Esercitazioni

-   [Creazione di funzioni di callback di stato](creating-status-callback-functions.md)

Funzioni necessarie per configurare l'operazione asincrona

-   [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funzioni che possono essere usate in modo asincrono

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnetti**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**Internetopenurl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Le [**funzioni FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)e [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) usano il valore di contesto fornito nella chiamata alla [**funzione InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

 

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server usare [Microsoft Windows servizi HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 