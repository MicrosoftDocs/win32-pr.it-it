---
description: 'Altre informazioni su: funzione JetCreateInstance'
title: Funzione JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319186"
---
# <a name="jetcreateinstance-function"></a>Funzione JetCreateInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>Funzione JetCreateInstance

La funzione **JetCreateInstance** alloca una nuova istanza del motore di database per l'utilizzo in un singolo processo.

**Windows XP: JetCreateInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Buffer di output che riceve l'istanza appena creata.

*szInstanceName*

Identificatore di stringa univoco per l'istanza da creare. Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.

**Nota** Un valore NULL viene considerato come un identificatore di stringa valido per un'istanza di. Solo un'istanza può avere un identificatore di stringa NULL.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>Il nome dell'istanza specificato è già in uso per questo processo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetCreateInstance</strong> quando <em>pinstance</em> è <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché non può essere usata quando il motore di database funziona in modalità a istanza singola (modalità di compatibilità di Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>Impossibile creare una nuova istanza. è stato raggiunto il numero massimo di istanze. Il numero massimo di istanze supportate viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, verrà allocata una nuova istanza e verrà restituito l'identificatore per esso. A questo punto, tutti i parametri di sistema per l'istanza avranno i valori dei parametri di sistema predefiniti globali. Una volta allocata, un'istanza deve essere terminata e/o liberata in un secondo momento.

In caso di errore, verrà restituito un errore che rappresenta la fonte di errore e non verrà allocata alcuna istanza.

#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a [JetInit](./jetinit-function.md) prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md). Il numero massimo di istanze che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato tramite una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Un'istanza è l'unità di recupero per il motore di database. Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Se la funzione ha esito positivo, il motore di database verrà automaticamente modificato in modalità a istanze diverse come effetto collaterale di questa chiamata. Se l'applicazione desidera consentire una sola istanza del processo, [JetInit](./jetinit-function.md) deve essere usato per avviare il motore di database in modalità di compatibilità con Windows 2000.

Se presente, il *szDisplayName* verrà usato per identificare l'istanza in posizioni come il registro eventi o verso altri chiamanti come le applicazioni di backup (tramite funzioni come [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Se il nome visualizzato non viene specificato, verrà usato il *szInstanceName* univoco, se presente, in caso contrario verrà restituita una stringa vuota. Se per il motore non è stata impostata la modalità in esecuzione, dopo questa chiamata verrà impostata la modalità a istanze diverse.

La sequenza di avvio tipica per un processo che potenzialmente esegue più istanze Jet è la seguente:

  - Una chiamata a [JetCreateInstance2](./jetcreateinstance2-function.md) che consente di allocare e assegnare un nome all'istanza.

  - Più chiamate a [JetSetSystemParameter](./jetsetsystemparameter-function.md) per tale istanza per impostare parametri di sistema diversi. Si noti che alcuni parametri di sistema devono essere univoci per ogni istanza, ad esempio [JET_paramSystemPath](./transaction-log-parameters.md) o [JET_paramLogFilePath](./transaction-log-parameters.md), quindi è molto probabile che sia necessario impostare ognuno di essi.

  - Avviare l'istanza utilizzando [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md). Per terminare e/o liberare un'istanza, è necessario usare [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .

Se questa è la prima istanza da avviare, verranno eseguiti alcuni passaggi aggiuntivi durante la chiamata per eseguire l'inizializzazione e la configurazione di base del sistema. Alcuni di questi passaggi potrebbero causare errori specifici che iniziano con JET_errOutOfMemory, ma anche altri. vedere gli errori precedenti.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
