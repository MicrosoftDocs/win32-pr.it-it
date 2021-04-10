---
title: Operazione asincrona
description: In modalità asincrona, un'applicazione può eseguire qualsiasi funzione che include un valore di contesto come uno dei relativi parametri e può continuare a eseguire altri comandi o funzioni mentre l'applicazione attende che la funzione completi la relativa attività.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7e1d0cf84aa92691e1d926d771ea809d31a171
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728930"
---
# <a name="asynchronous-operation"></a>Operazione asincrona

Il tempo impiegato da un'applicazione per accedere a una risorsa Internet dipende da diversi fattori, ad esempio la connessione utilizzata, il server in cui si trova la risorsa e il numero di utenti che tentano di accedere alla risorsa. Per le applicazioni che scaricano più risorse o gestiscono più attività (inclusi uno o più download), attendere il completamento di ogni download prima di procedere all'attività successiva può risultare estremamente inefficiente. Per ridurre la quantità di tempo di attesa di un'applicazione, molte delle funzioni WinINet possono funzionare in modo asincrono.

In modalità asincrona, un'applicazione può eseguire qualsiasi funzione che include un valore di contesto come uno dei relativi parametri e può continuare a eseguire altri comandi o funzioni mentre l'applicazione attende che la funzione completi la relativa attività. Durante il completamento dell'attività, una funzione di callback dello stato fornita dall'applicazione riceve una notifica sullo stato di avanzamento dell'attività e al suo completamento. A questo punto, la funzione di callback dello stato può chiamare altre funzioni o eseguire altre attività necessarie che dipendono dal completamento dell'attività.

Non esiste alcun thread di callback Afinity quando si chiama WinINet in modo asincrono: una chiamata può iniziare da un thread, ma qualsiasi altro thread può ricevere il callback.

-   [Vantaggi](#benefits)
-   [Scenari](#scenarios)
-   [Argomenti correlati](#related-topics)

## <a name="benefits"></a>Vantaggi

Il funzionamento asincrono presenta diversi vantaggi. Ad esempio:

-   Download simultaneo di più risorse Internet.

    È possibile connettersi a più risorse Internet contemporaneamente e scaricarle non appena diventano disponibili.

-   Miglioramento delle prestazioni dell'applicazione.

    Un'applicazione che usa le funzioni WinINet in modo asincrono non deve attendere il completamento della richiesta, pertanto l'applicazione è gratuita per eseguire altre attività che non dipendono dalla richiesta, migliorando così le prestazioni complessive dell'applicazione.

-   Monitorare lo stato del download.

    La funzione di callback di stato riceve notifiche durante l'elaborazione di una richiesta. Se necessario, l'applicazione può utilizzare le informazioni fornite da tale funzione di callback dello stato per informare l'utente sullo stato di avanzamento dell'operazione o per interrompere le richieste che richiedono troppo tempo per essere completate.

## <a name="scenarios"></a>Scenari

Supponiamo che l'applicazione debba scaricare i prezzi dei caffè dal caffè rovinato & tè e i siti Fourth Coffee e confrontare i prezzi. Il sito Fourth Coffee è in genere caratterizzato da un tempo di risposta più lento, quindi l'applicazione dovrebbe scaricare prima di tutto le informazioni dalla rovina del caffè & tè.

Sono state sviluppate due versioni dell'applicazione. Uno funziona in modo sincrono, scaricando prima di tutto i prezzi dal sito Coffee Down & Tea, quindi i prezzi del sito Fourth Coffee. Il secondo funziona in modo asincrono, inviando richieste a entrambi i siti e scaricando i prezzi quando diventano disponibili.

Nella tabella seguente viene illustrato cosa accadrebbe se il sito Fourth Coffee fosse più veloce in un determinato giorno.



| Evento                                                            | Versione sincrona                        | Versione asincrona                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Avvio                                                            | Inviare la richiesta a una rovina caffè & tè      | Inviare richieste a un caffè rovinato & tè e Fourth Coffee |
| Richiesta dalla versione asincrona al quarto caffè completata | Attesa                                    | Scarica i prezzi da Fourth Coffee                       |
| Richiesta di caduta del caffè & tè completata                       | Scarica i prezzi da un caffè rovinato & tè | Scarica i prezzi da un caffè rovinato & tè               |
| Dopo il download dei prezzi del caffè & tè              | Invia richiesta a Fourth Coffee              | Confrontare i prezzi                                           |
| Confronto della versione asincrona completata                      | Attesa                                    | Operazione completata                                       |
| Richiesta dalla versione sincrona a Fourth Coffee completata  | Scarica i prezzi da Fourth Coffee         | n/d                                                      |
| Dopo aver scaricato i prezzi di Fourth Coffee                      | Confrontare i prezzi                             | n/d                                                      |
| Confronto della versione sincrona completata                       | Operazione completata                         | n/d                                                      |



 

Un altro esempio è costituito da un Web browser, ad esempio Microsoft Internet Explorer. Quando il browser Scarica una pagina, è spesso necessario scaricare altre risorse, ad esempio immagini e file audio. In modalità asincrona, la pagina e le risorse associate possono essere richieste simultaneamente e scaricate quando diventano disponibili, anziché richiedere e scaricare la pagina e ogni risorsa una alla volta.

## <a name="related-topics"></a>Argomenti correlati

Di seguito sono riportati i collegamenti correlati.

Esercitazioni

-   [Creazione di funzioni di callback di stato](creating-status-callback-functions.md)

Funzioni necessarie per configurare l'operazione asincrona

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funzioni che possono essere usate in modo asincrono

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
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
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Le funzioni [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)e [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) usano il valore di contesto fornito nella chiamata alla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .

 

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 