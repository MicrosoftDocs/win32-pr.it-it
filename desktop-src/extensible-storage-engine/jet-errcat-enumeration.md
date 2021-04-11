---
description: 'Altre informazioni su: Enumerazione JET_ERRCAT'
title: Enumerazione JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
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
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231812"
---
# <a name="jet_errcat-enumeration"></a>Enumerazione JET_ERRCAT

Categoria dell'errore. La gerarchia è la seguente: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemi di IO non sono temporanei. | |--JET_errcatResource | |--JET_errcatMemory//memoria insufficiente (tutte le varianti) | |--JET_errcatQuota | |--JET_errcatDisk//spazio su disco insufficiente (tutte le varianti) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//in genere causati da utenti malgestiti | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Errori che in genere possono verificarsi in qualsiasi momento a causa di condizioni incontrollabili. Spesso temporanea, ma non sempre. Ripristino: è probabile che venga effettuato un nuovo tentativo o alla fine di informare l'operatore.</td>
</tr>
<tr class="even">
<td></td>
<td>Fatal</td>
<td>Questo errore di ordinamento si verifica solo quando ESE rileva una condizione di errore così grave, che non è possibile continuare in un modo sicuro (spesso transazionale) e invece che i dati danneggiati generano errori di questa categoria. Ripristino: riavviare l'istanza o il processo. Se il problema persiste, informare l'operatore.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O gli errori provengono dal sistema operativo e sono fuori dal controllo di ESE, questo tipo di errore è probabilmente temporaneo, probabilmente non. Ripristino: Riprova. Se non viene risolto, richiedere all'operatore il problema del disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Risorsa</td>
<td>Si tratta di una categoria che indica una delle numerose condizioni possibili di esaurimento delle risorse.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memoria</td>
<td>Condizione di memoria esaurita classica. Ripristino: attendere qualche minuto e riprovare, liberare memoria o uscire.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Alcune &quot; &quot; risorse speciali sono in pool di una determinata dimensione, semplificando il rilevamento delle perdite di queste risorse. Ripristino: potrebbe richiedere modifiche minime al codice. Per poter essere rilevati durante lo sviluppo, l'applicazione deve avere un'azione di solo debug, ad esempio un'asserzione. Per il codice per la vendita al dettaglio, è consigliabile considerare questo errore, ad esempio l'errore della categoria di memoria e riprovare, liberare memoria o uscire dall'operazione.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Condizioni del disco insufficiente. Ripristino: è possibile riprovare più tardi nella speranza che lo spazio sia disponibile o richiedere all'operatore di liberare spazio su disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Data</td>
<td>Errore relativo ai dati.</td>
</tr>
<tr class="odd">
<td></td>
<td>Danneggiamento</td>
<td>Ho mangiato il mio disco rigido. Problemi di danneggiamento classici, spesso permanenti senza azioni correttive. Ripristino: eseguire il ripristino da un backup, ad esempio l'operazione di ripristino delle utilità ESE, che consente di recuperare solo i dati a sinistra/con perdita di dati. Inoltre, nel caso del ripristino (JetInit), potrebbe essere possibile eseguire il ripristino consentendo la perdita di dati.</td>
</tr>
<tr class="even">
<td></td>
<td>Incoerente</td>
<td>Si tratta di un problema simile al danneggiamento in quanto i file di database e/o di log si trovano in uno stato incoerente e non riconciliabile tra loro. Questo problema è spesso dovuto a una gestione non gestita da parte dell'applicazione o dell'amministratore. Ripristino: eseguire il ripristino da un backup, ad esempio l'operazione di ripristino delle utilità ESE, che consente di recuperare solo i dati a sinistra/con perdita di dati. Inoltre, nel caso del ripristino (JetInit), potrebbe essere possibile eseguire il ripristino consentendo la perdita di dati.</td>
</tr>
<tr class="odd">
<td></td>
<td>Frammentazione</td>
<td>Si tratta di una classe di errori in cui è stata eseguita una risorsa interna permanente. Ripristino: per gli errori del database, la deframmentazione non in linea risolverà il problema. per i file di log è necessario _innanzitutto_ ripristinare tutti i database collegati a una chiusura normale e quindi eliminare tutti i file di log e il checkpoint.</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Contenitore per l'utilizzo e lo stato.</td>
</tr>
<tr class="odd">
<td></td>
<td>Utilizzo</td>
<td>Errore di utilizzo classico. questo significa che il codice client non ha passato gli argomenti corretti all'API JET. Questo errore probabilmente non verrà ritentato. Recupero: in genere il codice client deve dichiarare () questa classe di errori non viene restituita, quindi i problemi possono essere rilevati durante lo sviluppo. Nella vendita al dettaglio, l'app avrà probabilmente una piccola opzione, ma restituirà il problema all'operatore.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Si tratta della classificazione per i diversi segnali che possono essere restituiti dall'API per descrivere lo stato del database. un caso classico è JET_errRecordNotFound, che può essere restituito da JetSeek () quando il record richiesto non è stato trovato. Ripristino: non è rilevante, dipende in larga misura dall'API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoleti</td>
<td>L'errore viene riconosciuto come un errore valido, ma non è previsto che venga restituito da questa versione dell'API.</td>
</tr>
<tr class="even">
<td></td>
<td>Max</td>
<td>Valore massimo per l'enumerazione. Questa operazione non deve essere utilizzata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
