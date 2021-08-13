---
description: 'Altre informazioni su: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bd72ecab62eeccb3ed7e586e2e793bdb9796f09a57686e70d9177eb496316760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254323"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Il **JET_ERRCAT** di costanti descrive classificazioni o categorie di errori di livello superiore. Questo gruppo di costanti consente alle applicazioni di definire il trattamento predefinito per una classificazione degli errori, anziché gestire ogni singolo caso di errore. Garantisce inoltre che l'applicazione non deve gestire nuove condizioni di errore incluse nelle classificazioni esistenti.

Nota: questa documentazione è basata su una versione preliminare di Extensible Archiviazione Engine. Queste informazioni sono soggette a modifiche.

Le **JET_ERRCAT** costanti sono disposte in una gerarchia specifica di condizioni e sottocondizioni, come indicato di seguito:

|--- errore |--- operazione(al) | |--- I/| |--- O irreversibile | |--- memoria | |--- memoria | |--- quota | |--- disco | |--- dati | |--- | |--- | |--- frammentazione | |--- | |--- |--- | |--- Stato |--- utilizzo |---

La tabella seguente elenca le **costanti JET_ERRCAT** e fornisce una descrizione e informazioni di ripristino, in base alle specifiche specifiche.

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
<td><p>Rappresenta gli errori che possono verificarsi in qualsiasi momento a causa di condizioni non verificabili e sono spesso temporanei. Se specificato, vedere sottocategorie.</p></td>
<td><p>Riprovare e, se l'errore persiste, informare l'operatore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Rappresenta gli errori irreversibili che, quando si verificano, creano un rischio che ESE non possa continuare in modo sicuro (spesso transazionale) e che i dati potrebbero essere danneggiati.</p></td>
<td><p>Riavviare l'istanza o il processo. Se il problema persiste, informare l'operatore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Rappresenta gli errori di I/O, che provengono dal sistema operativo e non sono sotto il controllo di ESE. Questo tipo di errore può essere temporaneo.</p></td>
<td><p>Riprovare e, se l'errore persiste, chiedere all'operatore di controllare il disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Rappresenta una categoria di errori correlati alla mancanza di condizioni delle risorse.</p></td>
<td><p>Vedere sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Rappresenta un errore causato dalla mancanza di memoria.</p></td>
<td><p>Riprovare dopo un periodo di tempo, liberare memoria o uscire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Alcune risorse speciali sono in pool di una determinata dimensione, rendendo più semplice &quot; &quot; rilevare le perdite di queste risorse.</p></td>
<td><p>L'applicazione deve <strong>assert()</strong> per rilevare questi problemi durante lo sviluppo. Tuttavia, nel codice di vendita al dettaglio, l'applicazione deve considerare questo come un errore di memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Rappresenta un errore causato dalla mancanza di spazio su disco.</p></td>
<td><p>Riprovare in un secondo momento per determinare se è disponibile più spazio su disco oppure chiedere all'operatore di liberare spazio su disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Rappresenta una categoria di primo livello per gli errori correlati ai dati.</p></td>
<td><p>Vedere sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Rappresenta un problema di danneggiamento, che spesso è permanente senza azioni correttive.</p></td>
<td><p>Eseguire il ripristino dal backup usando l'operazione di ripristino delle utilità ESE (questa operazione ripristina solo i dati rimasti/persi). Inoltre, quando si usa il metodo recovery(JetInit), è possibile eseguire il ripristino consentendo la perdita di dati . Per altre informazioni, vedere JET_bitReplayIgnoreLostLogs <a href="gg269296(v=exchg.10).md">.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Rappresenta un errore in cui il database e/o i file di log si trova in uno stato incoerente e non può essere riconciliato. Questo errore potrebbe essere causato da una gestione errata dell'applicazione o dell'amministratore.</p></td>
<td><p>Eseguire il ripristino dal backup usando l'operazione di ripristino delle utilità ESE , che ripristina solo i dati rimasti/persi. Anche nel caso dell'operazione <strong>di ripristino(JetInit),</strong> il ripristino può essere eseguito consentendo la perdita di dati . Per altre informazioni, vedere JET_bitReplayIgnoreLostLogs <a href="gg269296(v=exchg.10).md">.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Rappresenta una classe di errori in cui alcune risorse interne persistenti si sono esaurite.</p></td>
<td><p>Per gli errori del database, la deframmentazione offline risolverà il problema. Per i file di log, ripristinare prima tutti i database collegati in un arresto pulito e quindi eliminare tutti i file di log e il checkpoint.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Vedere sottocategorie.</p></td>
<td><p>Vedere sottocategorie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Rappresenta un errore di utilizzo. Il codice client non ha passato gli argomenti corretti all'API <strong>JET.</strong> Questo errore verrà mantenuto con un nuovo tentativo.</p></td>
<td><p>Il codice client deve usare il <strong>metodo Assert()</strong> per assicurarsi che questa classe di errori non sia restituita, quindi i problemi possono essere rilevati durante lo sviluppo. Nella vendita al dettaglio, l'applicazione deve notificare l'errore all'operatore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Rappresenta una classe di messaggi che l'API può restituire per descrivere lo stato del database. Ad esempio, il <a href="gg294103(v=exchg.10).md">metodo JetSeek()</a> potrebbe <strong>restituire</strong> JET_errRecordNotFound quando il record richiesto non è stato trovato.</p></td>
<td><p>Varia in base all'API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Rappresenta gli errori di una versione precedente del motore. Questi errori non devono essere restituiti dal motore corrente.</p></td>
<td><p>Sconosciuto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Costante che indica la fine dell'enumerazione .</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>

