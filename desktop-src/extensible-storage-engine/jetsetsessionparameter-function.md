---
description: 'Altre informazioni su: funzione JetSetSessionParameter'
title: JetSetSessionParameter (funzione)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966545"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter (funzione)


_**Si applica a:** Windows | Windows Server_

La funzione **JetSetSessionParameter** configura il motore di database.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parametri

*sesid*

Specifica la sessione da utilizzare per questa chiamata.

Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.

*sesparamid*

ID del parametro della sessione da impostare.

*pvParam*

Dati da impostare in questo parametro della sessione.

*cbParam*

Dimensione dei dati forniti.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>L'istanza è stata inizializzata tramite una chiamata alla funzione <a href="gg294068(v=exchg.10).md">JetInit</a> e questa operazione non può essere eseguita di conseguenza. Questa situazione può verificarsi quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica nel valore del parametro non può più influire sullo stato del motore di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>I parametri specificati per l'indice di tupla non sono validi. Questo errore viene restituito solo quando il parametro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> è impostato su un valore non valido. Per informazioni su questi parametri, vedere <a href="gg294119(v=exchg.10).md">parametri di indice</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa situazione può verificarsi quando si verifica quanto segue:</p>
<ul>
<li><p>L'ID parametro di sistema specificato non è valido o non è supportato.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con una stringa la cui lunghezza non era compresa nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della rappresentazione del percorso assoluto non rientra nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori integer con un numero intero non compreso nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID non valido o un set di flag <strong>LCMapString</strong> non supportato.</p></li>
<li><p>Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema dopo che è stata chiamata la funzione <a href="gg294068(v=exchg.10).md">JetInit</a> , il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</p></li>
<li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per il parametro di sistema.</p></li>
<li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per il parametro di sistema.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Il percorso di file system specificato non è valido. Questo errore può essere restituito da <strong>JetSetSessionParameter</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi. Ad esempio, il parametro <em>JET_paramSystemPath</em> può restituire l'errore. Per informazioni su questo parametro, vedere <a href="gg269235(v=exchg.10).md">parametri del log delle transazioni</a>.</p></td>
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
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p>
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</p>
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il parametro di sistema verrà impostato sul valore fornito.

In caso di errore, il valore del parametro di sistema rimarrà invariato.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
