---
description: 'Altre informazioni su: funzione JetStopServiceInstance2'
title: JetStopServiceInstance2 (funzione)
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752279"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2 (funzione)


_**Si applica a:** Windows | Windows Server_

La funzione **JetStopServiceInstance2** prepara un'istanza prima della sospensione e prepara un'istanza dopo Resume. Suspend e Resume sono stati di esecuzione del modello di ciclo di vita delle app di Windows Store.

La funzione **JetStopServiceInstance2** è stata introdotta in Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di destinazione. Il tipo di dati **JET_INSTANCE** è un handle per l'istanza del database da usare per una chiamata all'API Jet. Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .

*grbit*

Gruppo di bit che specifica uno o più valori elencati e definiti nella tabella seguente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Arresta tutti i servizi Extensible Storage Engine (ESE) per l'istanza di specificata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Arresta le attività di manutenzione in background specificate dal client riavviabili (ad esempio, B + deframmentazione albero).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Quiesces tutte le cache Dirty sul disco. Questo valore è asincrono e può essere annullato.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Riprende le operazioni StopService rilasciate in precedenza; ovvero riavvia il servizio. Questo valore può essere combinato con il parametro <em>grbits</em> per riprendere servizi specifici o con JET_bitStopServiceAll per riprendere tutti i servizi precedentemente arrestati. Questo bit può essere utilizzato solo per riprendere StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches. Se in precedenza è stato chiamato con JET_bitStopServiceAll, un tentativo di usare JET_bitStopServiceResume avrà esito negativo. Se il secondo passaggio di ripresa non viene chiamato, le prestazioni dell'applicazione risulteranno ridotte. In questa situazione il checkpoint viene mantenuto a zero.</p></td>
</tr>
</tbody>
</table>


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
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Questa funzione consente a un'applicazione JET di spostare la cache del database in uno stato pulito o quasi pulito (con l'I/O del sistema operativo), in modo che se l'applicazione venisse terminata, il ripristino sarebbe stato rapido. Questo approccio è preferibile rispetto alla chiusura di JET chiamando le funzioni [JetTerm](./jetterm-function.md) o [JetDetachDatabase](./jetdetachdatabase-function.md) , in modo che, in uno scenario più comune, l'applicazione sia semplicemente sospesa e in seguito l'applicazione disponga dell'intera cache ed è pronta per iniziare il prima possibile.

Se questa funzione ha esito positivo, prepara la cache del database per una sospensione imminente. Questa funzione Accoda il lavoro a un thread di lavoro in background e ritorna immediatamente al chiamante. La funzione deve essere chiamata in base al VisibilityNotice PLM anziché chiamare dal gestore dell'evento di sospensione dell'applicazione per assicurarsi che JET abbia il tempo di scaricamento dei buffer dirty prima che PLM sospenda/termina il processo. Internamente, JET attiva una distribuzione immediata della manutenzione del checkpoint dopo la modifica della configurazione (aggiornamento del checkpoint o questo nuovo bit di cache mettere in stato). Per ulteriori informazioni sugli eventi VisibilityNotice, vedere [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Questa funzione deve essere chiamata due volte. Viene chiamato dopo che l'applicazione riceve l'avviso di sospensione dal sistema operativo, ma prima che l'applicazione sia stata sospesa. Viene quindi chiamato nuovamente dopo che il sistema operativo riprende l'applicazione. Ad esempio:

Quando viene chiamato per sospendere: JET_ERR JET_API JetStopServiceInstance2 (istanza, JET_bitStopServiceQuiesceCaches);

Quando viene ripreso: JET_ERR JET_API JetStopServiceInstance2 (istanza, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Requisiti

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
<td><p>Richiede Windows Server 2012.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
