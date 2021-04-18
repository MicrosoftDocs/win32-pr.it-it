---
description: Cache AutoProxy
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Cache AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318199"
---
# <a name="autoproxy-cache"></a>Cache AutoProxy

La funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) esegue la ricerca del proxy automatica in base alle singole richieste per l'URL specificato. Se vengono restituiti più proxy, le applicazioni client devono testare ogni proxy prima di inviare la richiesta. per ulteriori informazioni, vedere la sezione [solo un server proxy attualmente supportata](autoproxy-issues-in-winhttp.md) nei problemi di AutoProxy in WinHTTP. Le informazioni contenute in questo argomento sono valide per le chiamate a **WinHttpGetProxyForUrl** quando il client specifica l'individuazione automatica del proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , facoltativamente, individua l'URL del proxy AutoProxy e Scarica lo script di AutoProxy da tale sito. WinHttp usa lo script di AutoProxy per individuare i server proxy. Sia l'URL del proxy AutoProxy che lo script di AutoProxy vengono memorizzati nella cache per la sessione specificata. Solo un URL e uno script di AutoProxy vengono memorizzati nella cache per ogni sessione. In genere, lo script e l'URL del proxy AutoProxy vengono memorizzati nella cache fino a quando non viene modificato l'indirizzo IP associato al computer. Se viene rilevato un nuovo indirizzo IP durante una chiamata a **WinHttpGetProxyForUrl**, la chiamata tenterà di individuare un nuovo URL di AutoProxy e di memorizzare nella cache i risultati. È necessario consentire un solo utente per sessione, in modo che i dati memorizzati nella cache non siano condivisi con altri utenti nel computer. Per ulteriori informazioni, vedere [Cenni preliminari sulle sessioni WinHTTP](winhttp-sessions-overview.md).

Se il servizio out-of-process è attivo quando viene chiamato [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , l'URL e lo script del proxy AutoProxy memorizzati nella cache sono disponibili per l'intero computer. Tuttavia, se viene usato il servizio out-of-process e il flag **fAutoLogonIfChallenged** nella struttura *pAutoProxyOptions* è true, l'URL e lo script di AutoProxy non vengono memorizzati nella cache. Pertanto, la chiamata di **WinHttpGetProxyForUrl** con il membro **FAutoLogonIfChallenged** impostato su **true** comporta operazioni di overhead aggiuntive che potrebbero influire sulle prestazioni. Per migliorare le prestazioni, è possibile usare i passaggi seguenti.

**Per migliorare le prestazioni**

1.  Chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con il parametro fAutoLogonIfChallenged impostato su **false**. L'URL e lo script di AutoProxy vengono memorizzati nella cache per le chiamate future a **WinHttpGetProxyForUrl**.
2.  Se il passaggio 1 ha esito negativo, con **errore errore di \_ \_ accesso \_ WinHTTP**, chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con il membro **fAutoLogonIfChallenged** impostato su **true**.

 

 



