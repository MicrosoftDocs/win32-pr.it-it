---
description: 'Altre informazioni su: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313139"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Il gruppo **JET_ERRCAT** di costanti descrive le classificazioni di livello superiore o le categorie di errori. Questo gruppo di costanti consente alle applicazioni di definire il trattamento predefinito per una classificazione degli errori, anziché gestire singolarmente ogni caso di errore. Garantisce inoltre che non sia necessario che l'applicazione gestisca le nuove condizioni di errore incluse nelle classificazioni esistenti.

Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile. Queste informazioni sono soggette a modifiche.

Le costanti **JET_ERRCAT** sono disposte in una gerarchia specifica di condizioni e sottocondizioni, come indicato di seguito:

|---Error |---Operation (al) | |---Fatal | |---IO | |---Resource | |---Memory | |---quota | |---disco | |---dati | |---danneggiamento | |---incoerente | |---frammentazione | |---API |---utilizzo |---stato

Nella tabella seguente sono elencate le costanti **JET_ERRCAT** e vengono fornite una descrizione e informazioni di ripristino, come applicabile.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Costante/valore</p></th>
<th><p>Descrizione</p></th>
<th><p>Ripristino</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>Categoria di errore non valida.</p></td>
<td><p>N/D.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>Categoria di primo livello (nessun errore deve essere di questa classe).</p></td>
<td><p>Vedere le costanti di errore specifiche.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Rappresenta gli errori che possono verificarsi in qualsiasi momento a causa di condizioni incontrollabili e sono spesso temporanei. Se specificato, vedere le sottocategorie.</p></td>
<td><p>Riprovare e, se l'errore persiste, informare l'operatore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Rappresenta gli errori irreversibili che, quando si verificano, creano un rischio che ESE non possa continuare in modo sicuro (spesso transazionale) e i dati potrebbero essere danneggiati.</p></td>
<td><p>Riavviare l'istanza o il processo. Se il problema persiste, informare l'operatore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Rappresenta gli errori di i/o, provenienti dal sistema operativo, e sono fuori dal controllo ESE. Questo tipo di errore può essere temporaneo.</p></td>
<td><p>Riprovare. se l'errore persiste, richiedere all'operatore di controllare il disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Rappresenta una categoria di errori correlati a condizioni di risorse insufficienti.</p></td>
<td><p>Vedere le sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Rappresenta un errore causato dalla mancanza di memoria.</p></td>
<td><p>Riprovare dopo un periodo di tempo, liberare memoria o uscire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Alcune &quot; &quot; risorse speciali sono in pool di una determinata dimensione, semplificando il rilevamento delle perdite di queste risorse.</p></td>
<td><p>L'applicazione deve <strong>dichiarare ()</strong> per rilevare questi problemi durante lo sviluppo. Tuttavia, nel codice per la vendita al dettaglio, l'applicazione deve considerarla come un errore di memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Rappresenta un errore causato dalla mancanza di spazio su disco.</p></td>
<td><p>Riprovare in seguito per determinare se è disponibile più spazio su disco o richiedere all'operatore di liberare spazio su disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Rappresenta una categoria di primo livello per gli errori correlati ai dati.</p></td>
<td><p>Vedere le sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Rappresenta un problema di danneggiamento, che è spesso permanente senza azioni correttive.</p></td>
<td><p>Ripristino da backup tramite l'operazione di ripristino delle utilità ESE. questa operazione consente di ripristinare solo i dati a sinistra/con perdita di dati. Inoltre, quando si utilizza il metodo Recovery (JetInit), il ripristino può essere eseguito consentendo la perdita di dati. per ulteriori informazioni, vedere <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Rappresenta un errore in cui i file di database e/o di log si trovano in uno stato incoerente e non possono essere risolti. Questo errore potrebbe essere causato da un errore di gestione dell'applicazione o dell'amministratore.</p></td>
<td><p>Eseguire il ripristino da un backup tramite l'operazione di ripristino delle utilità ESE, che consente di ripristinare solo i dati a sinistra/con perdita di dati. Inoltre, nel caso dell'operazione di <strong>ripristino (JetInit)</strong> , il ripristino può essere eseguito consentendo la perdita di dati. per altre informazioni, vedere <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Rappresenta una classe di errori in cui è stata eseguita una risorsa interna permanente.</p></td>
<td><p>Per gli errori del database, la deframmentazione non in linea risolverà il problema. Per i file di log, è necessario innanzitutto ripristinare tutti i database collegati a una chiusura normale, quindi eliminare tutti i file di log e il checkpoint.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Vedere le sottocategorie.</p></td>
<td><p>Vedere le sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Rappresenta un errore di utilizzo. Il codice client non ha passato gli argomenti corretti all'API <strong>Jet</strong> . Questo errore verrà mantenuto con un nuovo tentativo.</p></td>
<td><p>Il codice client deve usare il metodo <strong>Assert ()</strong> per assicurarsi che questa classe di errori non venga restituita, quindi i problemi possono essere rilevati durante lo sviluppo. In dettaglio, l'applicazione deve notificare all'operatore l'errore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Rappresenta una classe di messaggi che l'API può restituire per descrivere lo stato del database. Ad esempio, il metodo <a href="gg294103(v=exchg.10).md">JetSeek ()</a> potrebbe restituire <strong>JET_errRecordNotFound</strong> quando il record richiesto non è stato trovato.</p></td>
<td><p>Varia a seconda dell'API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Rappresenta gli errori provenienti da una versione precedente del motore. Questi errori non devono essere restituiti dal motore corrente.</p></td>
<td><p>Sconosciuto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Costante che indica la fine dell'enumerazione.</p></td>
<td><p>N/D.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>

