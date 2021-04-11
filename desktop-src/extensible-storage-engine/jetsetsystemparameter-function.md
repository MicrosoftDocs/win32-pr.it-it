---
description: 'Altre informazioni su: funzione JetSetSystemParameter'
title: JetSetSystemParameter (funzione)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226248"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter (funzione)

La funzione **JetSetSystemParameter** viene utilizzata per impostare le numerose impostazioni di configurazione del motore di database.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Specifica l'istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Per Windows 2000, questo parametro viene ignorato e deve essere sempre **null**.

**Windows XP:**  Per Windows XP e versioni successive, questo parametro è leggermente sovraccarico. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **null** o può contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da un'istanza. Se il motore funziona in modalità a istanze diverse, questo parametro può essere **null** o un puntatore a un'istanza creata usando [JetInit](./jetinit-function.md) o [JetCreateIndex](./jetcreateindex-function.md). Se questo parametro è **null** , viene letta l'impostazione del parametro di sistema globale (o default). Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.

Anche se si tratta tecnicamente di un parametro out, questa API non modifica mai il contenuto del buffer fornito.

*sesid*

Specifica la sessione da utilizzare per questa chiamata.

Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.

*paramid*

ID del parametro di sistema che verrà impostato. Per un elenco completo dei parametri di sistema e delle relative proprietà, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .

*lParam*

Fornisce il valore da impostare per il parametro di sistema selezionato se il parametro di sistema è di tipo Integer.

*szParam*

Fornisce il valore per il parametro di sistema selezionato se il parametro di sistema è di tipo String.

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
<td><p>Operazione riuscita.</p>
<p><strong>Windows Vista:</strong>  In Windows Vista e versioni successive, è possibile restituire un esito positivo senza modificare il valore del parametro di sistema. Per ulteriori informazioni, vedere il JET_paramEnableAdvanced parametro System nell'argomento <a href="gg269346(v=exchg.10).md">meta Parameters</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>L'istanza è stata inizializzata tramite una chiamata a <a href="gg294068(v=exchg.10).md">JetInit</a> e non è possibile eseguire l'operazione di conseguenza. Questa situazione può verificarsi per <strong>JetSetSystemParameter</strong> quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica nel suo valore non può influire sullo stato del motore di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>I parametri specificati per l'indice di tupla non sono validi. Questo errore può essere restituito da <strong>JetSetSystemParameter</strong> solo quando si imposta <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetSetSystemParameter</strong> quando:</p>
<ul>
<li><p>L'ID parametro di sistema specificato non è valido o non è supportato.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con una stringa la cui lunghezza non rientra nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della rappresentazione del percorso assoluto non rientra nell'intervallo valido per il parametro.</p>
<p><strong>Windows Vista:</strong>  Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori integer con un numero intero non compreso nell'intervallo valido per il parametro.</p></li>
<li><p>È stato effettuato un tentativo di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>null</strong> , un LCID non valido o un set di flag LCMapString non supportato.</p>
<p><strong>Windows Vista:</strong>  Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</p></li>
<li><p>Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</p></li>
<li><p>È stato effettuato un tentativo di impostare un parametro di sistema dopo la chiamata di <a href="gg294068(v=exchg.10).md">JetInit</a> , il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</p></li>
<li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per il parametro di sistema.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</p></li>
<li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per il parametro di sistema.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Il percorso di file system specificato non è valido. Questo errore può essere restituito da <strong>JetSetSystemParameter</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi. Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> possibile che questo errore venga restituito.</p></td>
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
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p>
<p><strong>Windows Vista:</strong>  Questo errore verrà restituito solo da Windows Vista e versioni successive.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, l'impostazione per il parametro di sistema verrà impostata sul valore fornito.

In caso di errore, l'impostazione per il parametro di sistema rimarrà invariata.

#### <a name="remarks"></a>Commenti

**JetSetSystemParameter** esegue un processo insufficiente per convalidare l'impostazione scelta per ogni parametro di sistema. È necessario prestare attenzione a non basarsi su questa convalida per applicare impostazioni valide. Prestare particolare attenzione alla descrizione di ogni parametro di sistema e attenersi alle linee guida per una corretta impostazione del parametro di sistema.

È necessario impostare sempre un set di parametri di sistema per garantire che il motore di database funzioni come previsto. In particolare, tutti i parametri di sistema che influiscono sul layout fisico dei file utilizzati dal motore di database devono essere sempre impostati. Per ulteriori informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).

Ogni parametro di sistema ha un valore predefinito. Questi valori predefiniti si sono evoluti nel tempo e sono piuttosto arbitrari. Si consiglia vivamente che un'applicazione valuti tutti i valori predefiniti per assicurarsi che siano appropriati. Se non sono appropriati, devono essere configurati dall'applicazione. Questo è importante poiché molti di questi parametri possono avere un notevole effetto sull'affidabilità, sulle prestazioni e sull'utilizzo delle risorse del motore di database.

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
<td><p>Implementato come <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
