---
description: 'Altre informazioni su: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 951c26d0b1576d565b90f3bceeef9eb835e4be45
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476847"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Il **JET_ERRCAT** di costanti descrive classificazioni o categorie di errori di livello superiore. Questo gruppo di costanti consente alle applicazioni di definire il trattamento predefinito per una classificazione degli errori, anziché gestire ogni singolo caso di errore. Garantisce inoltre che l'applicazione non deve gestire nuove condizioni di errore incluse nelle classificazioni esistenti.

Nota: questa documentazione è basata su una versione preliminare di Extensible Archiviazione Engine. Queste informazioni sono soggette a modifiche.

Le **JET_ERRCAT** costanti sono disposte in una gerarchia specifica di condizioni e sottocondizioni, come indicato di seguito:

|--- errore |--- operazioni | |--- | |--- | |--- operazioni irreversibili di I/O | |--- | |--- memoria | |--- quota | |--- disco | |--- dati | |--- | |--- frammentazione | |--- incoerente | |--- Stato |--- utilizzo |---

La tabella seguente elenca le **costanti JET_ERRCAT** e fornisce una descrizione e informazioni di ripristino, in base alle specifiche specifiche.


| <p>Costante/valore</p> | <p>Descrizione</p> | <p>Ripristino</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Categoria di errore non valida.</p> | <p>N/D.</p> | 
| <p>JET_errcatError 1</p> | <p>Categoria di primo livello (nessun errore deve essere di questa classe).</p> | <p>Vedere le costanti di errore specifiche.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Rappresenta gli errori che possono verificarsi in qualsiasi momento a causa di condizioni non verificabili e sono spesso temporanei. Se specificato, vedere sottocategorie.</p> | <p>Riprovare e, se l'errore persiste, informare l'operatore.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Rappresenta gli errori irreversibili che, quando si verificano, creano un rischio che ESE non possa continuare in modo sicuro (spesso transazionale) e che i dati potrebbero essere danneggiati.</p> | <p>Riavviare l'istanza o il processo. Se il problema persiste, informare l'operatore.</p> | 
| <p>JET_errcatIO 4</p> | <p>Rappresenta gli errori di I/O, che provengono dal sistema operativo e non sono sotto il controllo di ESE. Questo tipo di errore può essere temporaneo.</p> | <p>Riprovare e, se l'errore persiste, chiedere all'operatore di controllare il disco.</p> | 
| <p>JET_errcatResource 5</p> | <p>Rappresenta una categoria di errori correlati alla mancanza di condizioni delle risorse.</p> | <p>Vedere sottocategorie.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Rappresenta un errore causato dalla mancanza di memoria.</p> | <p>Riprovare dopo un periodo di tempo, liberare memoria o uscire.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Alcune risorse "speciali" sono in pool di una determinata dimensione, rendendo più semplice rilevare le perdite di queste risorse.</p> | <p>L'applicazione deve <strong>assert()</strong> per rilevare questi problemi durante lo sviluppo. Tuttavia, nel codice di vendita al dettaglio, l'applicazione deve considerare questo come un errore di memoria.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Rappresenta un errore causato dalla mancanza di spazio su disco.</p> | <p>Riprovare in un secondo momento per determinare se è disponibile più spazio su disco oppure chiedere all'operatore di liberare spazio su disco.</p> | 
| <p>JET_errcatData 9</p> | <p>Rappresenta una categoria di primo livello per gli errori correlati ai dati.</p> | <p>Vedere sottocategorie.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Rappresenta un problema di danneggiamento, che spesso è permanente senza azioni correttive.</p> | <p>Eseguire il ripristino dal backup usando l'operazione di ripristino delle utilità ESE (questa operazione ripristina solo i dati rimasti/persi). Inoltre, quando si usa il metodo recovery(JetInit), è possibile eseguire il ripristino consentendo la perdita di dati. Per altre informazioni, vedere <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Rappresenta un errore in cui il database e/o i file di log si trova in uno stato incoerente e non può essere riconciliato. Questo errore potrebbe essere causato da una gestione errata dell'applicazione o dell'amministratore.</p> | <p>Eseguire il ripristino dal backup usando l'operazione di ripristino delle utilità ESE , che ripristina solo i dati rimasti/persi. Anche nel caso dell'operazione <strong>di ripristino(JetInit),</strong> il ripristino può essere eseguito consentendo la perdita di dati . Per altre informazioni, vedere JET_bitReplayIgnoreLostLogs <a href="gg269296(v=exchg.10).md">.</a></p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Rappresenta una classe di errori in cui alcune risorse interne persistenti si sono esaurite.</p> | <p>Per gli errori del database, la deframmentazione offline risolverà il problema. Per i file di log, ripristinare prima tutti i database collegati in un arresto pulito e quindi eliminare tutti i file di log e il checkpoint.</p> | 
| <p>JET_errcatApi 13</p> | <p>Vedere sottocategorie.</p> | <p>Vedere sottocategorie.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Rappresenta un errore di utilizzo. Il codice client non ha passato gli argomenti corretti all'API <strong>JET.</strong> Questo errore verrà mantenuto con un nuovo tentativo.</p> | <p>Il codice client deve usare <strong>il metodo Assert()</strong> per assicurarsi che questa classe di errori non sia restituita, quindi i problemi possono essere rilevati durante lo sviluppo. Nella vendita al dettaglio, l'applicazione deve notificare l'errore all'operatore.</p> | 
| <p>JET_errcatState 15</p> | <p>Rappresenta una classe di messaggi che l'API può restituire per descrivere lo stato del database. Ad esempio, il <a href="gg294103(v=exchg.10).md">metodo JetSeek()</a> potrebbe <strong>restituire</strong> JET_errRecordNotFound quando il record richiesto non è stato trovato.</p> | <p>Varia in base all'API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Rappresenta gli errori di una versione precedente del motore. Questi errori non devono essere restituiti dal motore corrente.</p> | <p>Sconosciuto.</p> | 
| <p>JET_errcatMax 17</p> | <p>Costante che indica la fine dell'enumerazione .</p> | <p>N/D.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows 8 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


