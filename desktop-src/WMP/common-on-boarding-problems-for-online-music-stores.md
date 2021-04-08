---
title: Problemi comuni di onboarding per gli archivi musicali online
description: Problemi comuni di onboarding per gli archivi musicali online
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f600d1035e0fd20be7786af4d4ffed4482138a72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729386"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Problemi comuni di onboarding per gli archivi musicali online

Di seguito è riportato un elenco dei problemi comuni di caricamento di Windows Media Player da evitare. Uno di questi problemi può causare l'esito negativo dei test di convalida dell'archivio. Se si verifica un errore, il passaggio RC2 rimanderà l'avvio fino alla successiva finestra di avvio disponibile.

1.  Errore di transizione dai server di prova ai server di produzione
    -   Pagine mancanti
    -   Impostazioni IIS (accesso, directory principali virtuali, HTTPS o altre impostazioni di sicurezza)
    -   Gli account di test non funzionano più.
    -   Per gli account di test non sono applicati crediti.
    -   I logo ospitati dal servizio non vengono spostati.
    -   Sono state rilevate restrizioni IP in precedenza. In particolare, i sistemi di e-commerce potrebbero avere un set di restrizioni diverso dal sito musica.
    -   Il documento ServiceInfo non viene aggiornato in modo da puntare alla produzione.
2.  Il collegamento di acquisto (o collegamento a negozio) nell'area di riproduzione ora non è valido. Si tratta di un problema comunemente trascurato, che causerà l'esito negativo dell'archivio anche quando tutto il resto è in ordine operativo.
3.  I tester di Microsoft devono avere una potenza di acquisto adeguata. Il team di convalida di Microsoft eseguirà diversi scenari di acquisto che variano da piccoli acquisti a acquisti di dimensioni molto elevate. È necessario fornire un metodo ricaricabile che funga da consumer all'interno del negozio. Questa operazione può variare dalla fornitura di una serie di account tramite una carta di credito fittizia. Ad esempio, un archivio non riuscirà in RC2 se un tester di convalida tenta di acquistare un album ma ha solo un credito sufficiente per acquistare una singola traccia.
4.  Se si usano controlli ActiveX nelle pagine del servizio, assicurarsi che vengano installati e disinstallati in tutte le versioni applicabili di Windows. In caso contrario, si tratta di un problema tipico. Spesso gli sviluppatori e i tester di un negozio online hanno i controlli ActiveX registrati nei propri computer, ma dimenticano l'installazione dei controlli nel computer dell'utente.

    Se l'archivio installa un plug-in o un controllo ActiveX, è necessario fornire all'utente un modo semplice per disinstallarlo. Ad esempio, Microsoft ha recentemente rilevato che alcuni archivi in linea hanno installato controlli ActiveX in Windows Media Player 11 per Windows Vista che non possono essere rimossi tramite il menu Installazione applicazioni. Dopo alcune indagini, Microsoft ha scoperto che i controlli ActiveX potevano essere rimossi tramite Gestione componenti aggiuntivi in Internet Explorer. È importante comunicare (tramite un file della guida, almeno) la modalità di installazione e disinstallazione di controlli e plug-in ActiveX.

    Per ulteriori informazioni su come integrare lo Store con l'infrastruttura di sicurezza di Windows Vista, vedere l'articolo ["procedure consigliate e linee guida per lo sviluppo di applicazioni in un ambiente con privilegi minimi"](/previous-versions/aa905330(v=msdn.10)).

 

 