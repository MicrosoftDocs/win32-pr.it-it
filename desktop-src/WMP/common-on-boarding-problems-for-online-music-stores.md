---
title: Problemi comuni di on-boarding per Musica online
description: Problemi comuni di on-boarding per Musica online
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player Negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c4cb38f088f463d6bea8ca15b3a92cea9610cc8541f27d55c48df07f9286d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763961"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Problemi comuni di on-boarding per Musica online

Di seguito è riportato un elenco Windows Media Player problemi di on-boarding che è consigliabile evitare. Uno di questi problemi può causare l'esito negativo dei test di convalida nell'archivio. In caso di esito negativo del passaggio RC2, l'avvio verrà posticipato fino alla successiva finestra di avvio disponibile.

1.  Non è possibile eseguire la transizione dai server di test ai server di produzione
    -   Pagine mancanti
    -   Impostazioni iis (accesso, VRoot, https o altre impostazioni di sicurezza)
    -   Gli account di test non funzionano più.
    -   Agli account di test non sono applicati crediti.
    -   I logo ospitati dal servizio non vengono spostati.
    -   Le restrizioni IP già applicate in precedenza si verificano di nuovo. In particolare, i sistemi di e-commerce potrebbero avere un set diverso di restrizioni dal sito della musica.
    -   Il documento ServiceInfo non viene aggiornato per puntare alla produzione.
2.  Il collegamento Acquista (o il collegamento Negozio) nell'area Attualmente in riproduzione non è valido. Si tratta di un problema comunemente trascurato e causerà l'esito negativo dell'archivio anche quando tutto il resto è in ordine.
3.  I tester Microsoft devono disporre di potenza di acquisto adeguata. Il team di convalida di Microsoft eseguirà diversi scenari di acquisto, da piccoli acquisti ad acquisti di grandi dimensioni. È necessario fornire un modo per consentire loro di agire come consumer all'interno del negozio. Può spaziare dalla fornitura di un'ampia gamma di account fino alla fornitura di una carta di credito fittizia. Ad esempio, un negozio avrà esito negativo in RC2 se un tester di convalida tenta di acquistare un album, ma ha solo credito sufficiente per acquistare una singola traccia.
4.  Se si usano controlli ActiveX all'interno delle pagine del servizio, assicurarsi che siano installati e disinstallati in modo pulito, sia in tutte le versioni applicabili di Windows. In caso negativo, si tratta di un problema tipico. Spesso gli sviluppatori e i tester di un negozio online hanno i controlli ActiveX registrati nei propri computer, ma dimenticano di installare i controlli nel computer dell'utente.

    Se lo Store installa un plug-in o un controllo ActiveX, è necessario fornire all'utente un modo semplice per disinstallarlo. Microsoft ha rilevato, ad esempio, di recente che alcuni store online hanno installato controlli ActiveX in Windows Media Player 11 per Windows Vista che non è stato possibile rimuovere tramite il menu Installazione applicazioni. Dopo alcune indagini, Microsoft ha scoperto che i controlli ActiveX possono essere rimossi tramite Gestione componenti aggiuntivi in Internet Explorer. È importante comunicare (almeno tramite un file della Guida) il modo in cui installare e disinstallare i ActiveX e i plug-in.

    Per altre informazioni su come integrare l'archivio con l'infrastruttura di sicurezza in Windows Vista, vedere l'articolo "Procedure consigliate per gli sviluppatori e linee guida per le applicazioni in un ambiente con privilegi [minimi".](/previous-versions/aa905330(v=msdn.10))

 

 