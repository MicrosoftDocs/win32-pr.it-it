---
description: 'Altre informazioni su: funzione JetGetSystemParameter'
title: JetGetSystemParameter (funzione)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233356"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter (funzione)

La funzione **JetGetSystemParameter** legge le numerose impostazioni di configurazione del motore di database.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre **null**.

Per Windows XP e versioni successive, questo parametro è leggermente sovraccarico. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **null** o può contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da un'istanza. Se il motore funziona in modalità a istanze diverse, questo parametro può essere **null** o un puntatore a un'istanza creata utilizzando [JetInit](./jetinit-function.md) o [JetCreateInstance](./jetcreateinstance-function.md). Se questo parametro è **null** , viene letta l'impostazione del parametro di sistema globale (o default). Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.

*sesid*

Sessione da utilizzare per questa chiamata.

Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.

*paramid*

ID del parametro di sistema che verrà letto.

Per un elenco completo dei parametri di sistema e delle relative proprietà, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .

*plParam*

Buffer di output che riceve il valore del parametro di sistema selezionato se tale parametro di sistema è di tipo Integer.

*szParam*

Buffer di output che riceve il valore del parametro di sistema selezionato se tale parametro di sistema è di tipo String.

*cbMax*

Dimensione massima in byte del buffer di output della stringa.

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
<td><p>JET_errInitInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p>
<p>Questo problema può verificarsi per <strong>JetGetSystemParameter</strong> quando:</p>
<ul>
<li><p>L'ID parametro di sistema specificato non è valido o non è supportato.</p></li>
<li><p>Per il parametro di sistema specificato è necessario fornire il buffer di output di tipo integer e il puntatore del buffer di output è <strong>null</strong>.</p></li>
<li><p>Il parametro di sistema specificato richiede che venga fornito un buffer di output di stringa e che il puntatore del buffer di output sia <strong>null</strong>.</p>
<p><strong>Windows Vista:  </strong> Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</p></li>
<li><p>Il parametro di sistema specificato richiede che venga fornito un buffer di output di stringa e che la dimensione del buffer di output sia troppo piccola per accettare una stringa con terminazione null.</p>
<p><strong>Windows Vista:  </strong> Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</p></li>
<li><p>Impossibile leggere il parametro di sistema specificato perché è di sola scrittura.</p></li>
<li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di lettura di un valore specifico dell'istanza per il parametro di sistema. Questa operazione può essere eseguita solo in Windows XP e versioni successive.</p></li>
<li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di lettura del valore globale per il parametro di sistema. Questa operazione può essere eseguita solo in Windows XP e versioni successive.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance</p></td>
<td><p>L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p>
<p><strong>Windows Vista:  </strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</p>
<p>Il buffer di output è stato riempito con la maggior parte delle impostazioni del parametro di sistema. Se il buffer di output è di almeno un carattere di lunghezza, la stringa in tale buffer di output sarà terminata con null.</p>
<p><strong>Nota  </strong> Questo errore non viene restituito da tutte le versioni. Per ulteriori informazioni, vedere la sezione Osservazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>L'operazione non è riuscita perché il buffer di output era troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</p>
<p><strong>Nota  </strong> Questo errore non viene restituito in alcuni casi per mantenere la compatibilità delle applicazioni. Per ulteriori informazioni, vedere la sezione Osservazioni.</p>
<p><strong>Windows Vista:  </strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il buffer di output appropriato per il parametro di sistema richiesto verrà impostato sul valore di tale parametro di sistema.

In caso di errore, lo stato dei buffer di output sarà indefinito.

#### <a name="remarks"></a>Commenti

Si è verificato un problema importante in questa API presente in tutte le versioni. Se viene richiesto un parametro di sistema con un valore stringa e il buffer di output è troppo piccolo per ricevere l'intera impostazione del parametro di sistema, JET_wrnBufferTruncated non verrà restituito. Viene invece restituito JET_errSuccess. Se la lunghezza della stringa restituita è uguale alla dimensione del buffer di output minore del carattere di terminazione **null** , il chiamante deve reagire come se JET_wrnBufferTruncated fosse stato restituito. Se viene specificato un buffer di output di stringa di dimensioni zero, il chiamante deve reagire come se JET_errInvalidParameter fosse stato restituito.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
