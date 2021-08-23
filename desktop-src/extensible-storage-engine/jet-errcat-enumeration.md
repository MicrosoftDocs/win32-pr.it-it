---
description: 'Altre informazioni su: enumerazione JET_ERRCAT di dati'
title: JET_ERRCAT enumerazione (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f259edf0e087831cfb667caa5fa8dcf215638ab6d739812fa2e6208327a22f7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232801"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT enumerazione

Categoria di errore. La gerarchia è la seguente: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // problemi di I/O non è possibile, può essere temporaneo o meno. | |-- JET_errcatResource | |-- JET_errcatMemory // memoria insufficiente (tutte le varianti) | |-- JET_errcatQuota | |-- JET_errcatDisk // spazio su disco (tutte le varianti) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // in genere causato da errori di gestione | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Sconosciuto</td>
<td>Categoria sconosciuta.</td>
</tr>
<tr class="even">
<td></td>
<td>Errore</td>
<td>Categoria generica.</td>
</tr>
<tr class="odd">
<td></td>
<td>Operazione</td>
<td>Errori che in genere possono verificarsi in qualsiasi momento a causa di condizioni non verificabili. Spesso temporaneo, ma non sempre. Ripristino: probabilmente riprovare o alla fine informare l'operatore.</td>
</tr>
<tr class="even">
<td></td>
<td>Fatal</td>
<td>Questo errore di ordinamento si verifica solo quando ESE rileva una condizione di errore così grave che non è possibile continuare in modo sicuro (spesso transazionale) e invece di danneggiare i dati vengono generati errori di questa categoria. Ripristino: riavviare l'istanza o il processo. Se il problema persiste, informare l'operatore.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>Gli errori O provengono dal sistema operativo e sono fuori controllo di ESE. Questo tipo di errore è probabilmente temporaneo, probabilmente no. Ripristino: riprovare. Se non viene risolto, chiedere all'operatore informazioni sul problema del disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Risorsa</td>
<td>Si tratta di una categoria che indica una delle numerose potenziali condizioni di out-of-resource.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memoria</td>
<td>Condizione classica di memoria insufficiente. Ripristino: attendere un po' e riprovare, liberare memoria o uscire.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Alcune risorse speciali sono in pool di una determinata dimensione, rendendo più semplice &quot; &quot; rilevare le perdite di queste risorse. Ripristino: potrebbe essere necessario apportare alcune modifiche minori al codice. L'applicazione deve avere un'azione di solo debug, ad esempio assert, in queste condizioni per rilevarle durante lo sviluppo. Per il codice di vendita al dettaglio, è consigliabile considerare questo errore come l'errore di categoria Memoria e riprovare, liberare memoria o uscire dall'operazione.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Condizioni del disco insufficiente. Ripristino: è possibile riprovare in un secondo momento nella speranza che sia disponibile più spazio oppure chiedere all'operatore di liberare spazio su disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Dati</td>
<td>Errore correlato ai dati.</td>
</tr>
<tr class="odd">
<td></td>
<td>Corruzione</td>
<td>Il disco rigido mi ha fatto i compiti. Problemi di danneggiamento classici, spesso permanenti senza azioni correttive. Ripristino: eseguire il ripristino dal backup, ad esempio l'operazione di ripristino delle utilità ese (che recupera solo i dati rimasti/persi). Anche nel caso del ripristino (JetInit) è possibile eseguire il ripristino consentendo la perdita di dati.</td>
</tr>
<tr class="even">
<td></td>
<td>Incoerente</td>
<td>Questo comportamento è simile al danneggiamento perché i file di database e/o di log sono in uno stato incoerente e non riconciliabile tra loro. Spesso ciò è causato da una gestione errata dell'applicazione o dell'amministratore. Ripristino: ripristino da backup, ad esempio l'operazione di ripristino delle utilità ese (che recupera solo i dati rimasti/persi). Anche nel caso del ripristino (JetInit) è possibile eseguire il ripristino consentendo la perdita di dati.</td>
</tr>
<tr class="odd">
<td></td>
<td>Frammentazione</td>
<td>Si tratta di una classe di errori in cui alcune risorse interne persistenti si sono esaurite. Ripristino: per gli errori del database, la deframmentazione  offline correggerà il problema, perché i file di log ripristinano prima tutti i database collegati a un arresto pulito e quindi eliminano tutti i file di log e il checkpoint.</td>
</tr>
<tr class="even">
<td></td>
<td>Api</td>
<td>Contenitore per Usage e State.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uso</td>
<td>Errore di utilizzo classico, ciò significa che il codice client non ha passato argomenti corretti all'API JET. Questo errore probabilmente non verrà restituito con un nuovo tentativo. Ripristino: in genere il codice client deve essere Assert() che questa classe di errori non viene restituita, quindi i problemi possono essere rilevati durante lo sviluppo. Nella vendita al dettaglio, l'app avrà probabilmente poche opzioni, ma per restituire il problema all'operatore.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Questa è la classificazione per diversi segnali che l'API potrebbe restituire descrivere lo stato del database, un caso classico è JET_errRecordNotFound che può essere restituito da JetSeek() quando il record richiesto non è stato trovato. Ripristino: non è realmente rilevante, dipende notevolmente dall'API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoleti</td>
<td>L'errore viene riconosciuto come errore valido, ma non deve essere restituito da questa versione dell'API.</td>
</tr>
<tr class="even">
<td></td>
<td>Max</td>
<td>Valore massimo per l'enumerazione . Questo non deve essere usato.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
