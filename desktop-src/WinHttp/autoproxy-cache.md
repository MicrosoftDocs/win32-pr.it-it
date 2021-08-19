---
description: Cache del proxy automatico
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Cache del proxy automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d494f1491dd52484a893dbab601ed4870f03badf5f849dca413f9554a8493e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614181"
---
# <a name="autoproxy-cache"></a>Cache del proxy automatico

La [**funzione WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) esegue la ricerca del proxy automatico per ogni richiesta per l'URL specificato. Se vengono restituiti più proxy, le applicazioni client devono testare ogni proxy prima di inviare la richiesta. Per altre informazioni, vedere la sezione È attualmente supportato un solo [server proxy](autoproxy-issues-in-winhttp.md) in Problemi del proxy automatico in WinHTTP. Le informazioni contenute in questo argomento si applicano alle chiamate **a WinHttpGetProxyForUrl** quando il client specifica l'individuazione automatica del proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) individua facoltativamente l'URL del proxy automatico e scarica lo script del proxy automatico da tale sito. WinHttp usa lo script autoproxy per individuare i server proxy. Sia l'URL del proxy automatico che lo script del proxy automatico vengono memorizzati nella cache per la sessione specificata. Solo un URL e uno script del proxy automatico vengono memorizzati nella cache per ogni sessione. In genere, lo script e l'URL del proxy automatico vengono memorizzati nella cache fino a quando non cambia l'indirizzo IP associato al computer. Se durante una chiamata a **WinHttpGetProxyForUrl** viene rilevato un nuovo indirizzo IP, la chiamata tenterà di individuare un nuovo URL e script del proxy automatico e memorizzare nella cache i risultati. Deve essere consentito un solo utente per sessione, in modo che i dati memorizzati nella cache non siano condivisi con altri utenti del computer. Per altre informazioni, vedere [Cenni preliminari sulle sessioni WinHTTP.](winhttp-sessions-overview.md)

Se il servizio out-of-process è attivo quando viene chiamato [**WinHttpGetProxyForUrl,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) l'URL e lo script del proxy automatico memorizzati nella cache sono disponibili per l'intero computer. Tuttavia, se viene usato il servizio out-of-process e il flag **fAutoLogonIfChallenged** nella struttura *pAutoProxyOptions* è true, l'URL e lo script del proxy automatico non vengono memorizzati nella cache. Pertanto, la chiamata **di WinHttpGetProxyForUrl** con il membro **fAutoLogonIfChallenged** impostato su **TRUE** comporta operazioni aggiuntive di overhead che possono influire sulle prestazioni. I passaggi seguenti possono essere usati per migliorare le prestazioni.

**Per migliorare le prestazioni**

1.  Chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con il parametro fAutoLogonIfChallenged impostato su **false.** L'URL e lo script del proxy automatico vengono memorizzati nella cache per le chiamate future **a WinHttpGetProxyForUrl.**
2.  Se il passaggio 1 ha esito negativo, con **ERRORE \_ WINHTTP \_ LOGIN \_ FAILURE**, chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) con il membro **fAutoLogonIfChallenged** impostato su **TRUE.**

 

 



