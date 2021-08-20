---
description: Altre informazioni sulla funzione JetSetSessionParameter
title: Funzione JetSetSessionParameter
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
ms.openlocfilehash: 5766a503fbac8a8abae51c6022fe91e9ecca0d72e28cbecbaeed597862765bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891019"
---
# <a name="jetsetsessionparameter-function"></a>Funzione JetSetSessionParameter


_**Si applica a:** Windows | Windows Server_

La **funzione JetSetSessionParameter** configura il motore di database.

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

Se specificato, l'istanza specificata viene ignorata e verrà usata l'istanza associata alla sessione.

*sesparamid*

ID del parametro di sessione da impostare.

*pvParam*

Dati da impostare in questo parametro di sessione.

*cbParam*

Dimensioni dei dati forniti.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE (Extensible Archiviazione Engine), vedere [Errori](./extensible-storage-engine-errors.md) del motore di Archiviazione estendibile e Parametri [di gestione degli errori](./error-handling-parameters.md).

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
<td><p>L'istanza è stata inizializzata usando una chiamata alla <a href="gg294068(v=exchg.10).md">funzione JetInit</a> e questa operazione non può essere eseguita di conseguenza. Ciò può verificarsi quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica del valore del parametro non può più influire sullo stato del motore di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>I parametri dell'indice di tupla specificati non sono validi. Questo errore viene restituito solo <em>quando il parametro JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> è impostato su un valore non valido. Per informazioni su questi parametri, vedere <a href="gg294119(v=exchg.10).md">Parametri di indice</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi quando si verifica quanto segue:</p>
<ul>
<li><p>L'ID del parametro di sistema specificato non è valido o non è supportato.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori stringa con una stringa la cui lunghezza non rientra nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della relativa rappresentazione del percorso assoluto non rientra nell'intervallo valido per tale parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori integer con un numero intero non compreso nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Null, un LCID non valido o un set non supportato di flag <strong>LCMapString.</strong></p></li>
<li><p>Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema dopo la chiamata della funzione <a href="gg294068(v=exchg.10).md">JetInit,</a> il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</p></li>
<li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per tale parametro di sistema.</p></li>
<li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per tale parametro di sistema.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Il percorso file system specificato non è valido. Questo errore può essere restituito da <strong>JetSetSessionParameter solo</strong> quando si impostano parametri di sistema che rappresentano file system percorsi. Ad esempio, il <em>parametro JET_paramSystemPath</em> può restituire questo errore. Per informazioni su questo parametro, vedere <a href="gg269235(v=exchg.10).md">Parametri del log delle transazioni</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p>
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>L'handle dell'istanza non è valido o fa riferimento a un'istanza arrestata.</p>
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il parametro di sistema verrà impostato sul valore fornito.

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


#### <a name="see-also"></a>Vedi anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
