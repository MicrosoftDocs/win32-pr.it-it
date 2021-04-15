---
description: 'Altre informazioni su: funzione JetSetLS'
title: Funzione JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525555"
---
# <a name="jetsetls-function"></a>Funzione JetSetLS


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetls-function"></a>Funzione JetSetLS

La funzione **JetSetLS** consente all'applicazione di associare un handle di contesto noto come archiviazione locale con un cursore o la tabella associata a tale cursore. Questo handle di contesto può essere utilizzato dall'applicazione per archiviare dati ausiliari associati a un cursore o a una tabella. In seguito, l'applicazione riceve una notifica tramite un callback di runtime quando è necessario rilasciare l'handle del contesto. Ciò consente di associare lo stato allocato in modo dinamico a un cursore o a una tabella.

**Windows XP:**  **JetSetLS** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*ls*

Handle di contesto da associare al cursore o alla tabella.

Quando si specifica JET_bitLSReset, il valore effettivo di questo parametro viene ignorato e viene utilizzato JET_LSNil.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSCursor</p></td>
<td><p>Questa opzione indica che l'handle di contesto deve essere associato al cursore specificato.</p>
<p>Se non viene specificato né JET_bitLSCursor né JET_bitLSTable, JET_bitLSCursor si presume.</p>
<p>Non è consentito usare questa opzione con JET_bitLSTable. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>Questa opzione indica che l'handle del contesto specificato deve essere ignorato e che l'handle di contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil.</p>
<p>È importante tenere presente che questa azione non comporterà la pulizia del valore precedente dell'handle di contesto per l'oggetto scelto da parte di un callback. La pulizia corretta dell'handle di contesto precedente può essere eseguita usando <a href="gg269234(v=exchg.10).md">JetGetLS</a> con JET_bitLSReset. Per ulteriori informazioni, vedere <a href="gg269234(v=exchg.10).md">JetGetLS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Questa opzione indica che l'handle di contesto deve essere associato alla tabella associata al cursore specificato.</p>
<p>Non è consentito usare questa opzione con JET_bitLSCursor. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p></td>
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
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida, è stata usata in modo errato o non è stata implementata. Questo problema può verificarsi per <strong>JetSetLS</strong> quando vengono specificati entrambi JET_bitLSCursor e JET_bitLSTable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>Impossibile associare l'handle del contesto specificato all'oggetto richiesto perché è già associato a un handle di contesto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>Impossibile associare l'handle del contesto specificato all'oggetto richiesto perché il callback di runtime non è stato configurato per l'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, l'handle di contesto specificato è stato associato correttamente all'oggetto richiesto. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, non sono state apportate modifiche allo stato dell'oggetto richiesto. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

L'archiviazione locale per un cursore o una tabella deve essere visualizzata come cache volatile. L'applicazione deve prima provare a recuperare l'handle del contesto usando [JetGetLS](./jetgetls-function.md). Se il valore non è impostato (ovvero è JET_LSNil), l'applicazione deve creare un nuovo contesto e caricarlo nella cache usando **JetSetLS**. L'applicazione può ripulire la cache utilizzando una chiamata a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Se il motore di database elimina la cache, verrà generato un callback di runtime per concedere all'applicazione la possibilità di pulire tale contesto. Il tipo di callback verrà JET_cbtypFreeCursorLS per un handle di contesto associato a un cursore e JET_cbtypFreeTableLS per un handle di contesto associato a una tabella. In entrambi i casi, l'handle di contesto verrà passato come pvArg1. Per ulteriori informazioni, vedere [JET_CALLBACK](./jet-callback-callback-function.md) .

Il callback di runtime deve essere configurato correttamente per l'istanza associata alla sessione specificata prima di poter usare l'archiviazione locale. Questo callback può essere impostato usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramRuntimeCallback](./callback-parameters.md). Per ulteriori informazioni, vedere [JetSetSystemParameter](./jetsetsystemparameter-function.md) e [JET_paramRuntimeCallback](./callback-parameters.md) nei parametri di sistema.

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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
