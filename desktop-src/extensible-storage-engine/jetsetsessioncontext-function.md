---
description: Altre informazioni sulla funzione JetSetSessionContext
title: Funzione JetSetSessionContext
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
ms.openlocfilehash: f76d6e73c3e9b40a1417acb953ea4342628844105c62ed74284efeaa60ea1a70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780421"
---
# <a name="jetsetsessioncontext-function"></a>Funzione JetSetSessionContext


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>Funzione JetSetSessionContext

La **funzione JetSetSessionContext** associa una sessione al thread corrente usando l'handle di contesto specificato. Questa associazione sostituisce il requisito predefinito del motore in base al cui thread deve essere eseguita una transazione per una determinata sessione.

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

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto. Questo errore verrà restituito <strong>da JetSetSessionContext</strong> nelle condizioni seguenti:</p>
<ul>
<li><p><em>ulContext</em> è NULL</p></li>
<li><p><em>ulContext</em> è -1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextAlreadySet</p></td>
<td><p>Impossibile associare la sessione al thread corrente perché è già stata associata a un thread.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, la sessione verrà associata al thread corrente. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, lo stato della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Una sessione è in genere associata a un thread specifico per la durata di una transazione. Questo comportamento è progettato per consentire alle applicazioni di rilevare e impedire la condivisione concettualmente non consigliata di una singola sessione tra più thread. In alcuni casi, questo semplice controllo non funziona con l'architettura dell'applicazione. Ad esempio, se l'applicazione ospita oggetti lato server usando un pool di thread e le transazioni si estendono su più chiamate del server a un determinato oggetto, questa protezione può causare l'esito negativo di alcune di queste chiamate con JET_errSessionSharingViolation anche se il modello di utilizzo è corretto. Questa situazione è comune per i server oggetti COM.

**JetSetSessionContext e** [JetResetSessionContext](./jetresetsessioncontext-function.md) risolvono questo problema rendendo questo controllo di condivisione della sessione un po' più flessibile. Quando l'applicazione inizia a effettuare una serie di chiamate API ESE usando una sessione specifica, imposta prima di tutto il contesto della sessione su un valore specificato. Questa azione associa la sessione al thread chiamante. Nell'esempio specificato, questo contesto potrebbe essere l'indirizzo dell'oggetto che contiene l'handle di sessione JET. Dopo aver effettuato le chiamate API ESE, l'applicazione reimposta il contesto della sessione. Questa azione disassocia la sessione dal thread chiamante. L'oggetto e la relativa sessione possono quindi essere utilizzati da un altro thread anche se la sessione ha una transazione attiva.

È importante notare che è necessario **chiamare JetSetSessionContext** prima di aprire una transazione in tale sessione, perché l'associazione non funzionerà.

**JetSetSessionContext** è thread-safe. Più thread possono provare a impostare un contesto di thread nella stessa sessione contemporaneamente e ne verrà vinto solo uno. Questo fatto può essere usato dall'applicazione come mezzo per allocare una sessione da un pool senza archiviare lo stato esterno sulla relativa allocazione.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
