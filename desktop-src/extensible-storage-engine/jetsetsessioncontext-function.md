---
description: 'Altre informazioni su: funzione JetSetSessionContext'
title: JetSetSessionContext (funzione)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307807"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext (funzione)

La funzione **JetSetSessionContext** associa una sessione al thread corrente usando l'handle di contesto specificato. Questa associazione esegue l'override del requisito del motore predefinito che una transazione per una determinata sessione deve essere interamente eseguita sullo stesso thread.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*ulContext*

Identificatore univoco a cui verrà associata la sessione.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto. Questo errore viene restituito da <strong>JetSetSessionContext</strong> nelle condizioni seguenti:</p>
<ul>
<li><p><em>ulContext</em> è null</p></li>
<li><p><em>ulContext</em> è-1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextAlreadySet</p></td>
<td><p>Impossibile associare la sessione al thread corrente perché è già stata associata a un thread.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, la sessione verrà associata al thread corrente. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, lo stato della sessione rimarrà invariato. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Una sessione è in genere associata a un thread specifico per la durata di una transazione. Questo comportamento è progettato per aiutare le applicazioni a rilevare ed evitare la condivisione concettualmente non consigliata di una singola sessione tra più thread. In alcuni casi questo semplice controllo non funziona con l'architettura dell'applicazione. Se, ad esempio, l'applicazione ospita oggetti lato server utilizzando un pool di thread e le transazioni si estendono su più chiamate server a un determinato oggetto, questa protezione potrebbe causare l'esito negativo di alcune chiamate con JET_errSessionSharingViolation anche se il modello di utilizzo è corretto. Questa situazione è comune per i server oggetto COM.

**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) risolvono questo problema rendendo il controllo della condivisione della sessione leggermente più flessibile. Quando l'applicazione inizia a eseguire una serie di chiamate API ESE usando una determinata sessione, imposta prima di tutto il contesto della sessione su un valore specificato. Questa azione associa la sessione al thread chiamante. Nell'esempio specificato, questo contesto può essere l'indirizzo dell'oggetto che contiene l'handle della sessione JET. Una volta effettuate le chiamate all'API ESE, l'applicazione Reimposta il contesto della sessione. Questa azione annulla l'associazione della sessione dal thread chiamante. L'oggetto e la relativa sessione possono quindi essere utilizzati da un altro thread anche se la sessione dispone di una transazione attiva.

È importante notare che **JetSetSessionContext** deve essere chiamato prima di aprire una transazione nella sessione o l'associazione non funzionerà.

**JetSetSessionContext** è thread-safe. Più thread possono provare a impostare un contesto di thread nella stessa sessione nello stesso momento e solo uno vincerà. Questo fatto può essere utilizzato dall'applicazione come mezzo per allocare una sessione da un pool senza archiviare lo stato esterno sulla relativa allocazione.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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


#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
