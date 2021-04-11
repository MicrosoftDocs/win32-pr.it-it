---
description: 'Altre informazioni su: funzione JetTerm2'
title: Funzione JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129718"
---
# <a name="jetterm2-function"></a>Funzione JetTerm2


_**Si applica a:** Windows | Windows Server_

## <a name="jetterm2-function"></a>Funzione JetTerm2

La funzione **JetTerm2** avvia l'arresto di un'istanza che è stata inizializzata da [JetInit](./jetinit-function.md).

**JetTerm2** può anche eliminare un'istanza non inizializzata creata da [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **null**.

**Windows XP e versioni successive:**  Questo parametro è sovraccarico. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **null** o potrebbe contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). Se il motore funziona in modalità a istanze diverse, questo parametro deve essere un puntatore a un'istanza creata con [JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei valori seguenti.

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
<td><p>JET_bitTermComplete</p></td>
<td><p>Richiede che l'istanza venga arrestata in modo corretto. Eventuali operazioni di pulizia facoltative normalmente eseguite in background in fase di esecuzione vengono completate immediatamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>Richiede che l'istanza venga arrestata nel minor tempo possibile. Qualsiasi lavoro facoltativo che normalmente verrebbe eseguito in background in fase di esecuzione viene abbandonato.</p>
<p><strong>Nota</strong>  Questa opzione può causare una perdita di spazio temporanea o permanente nel database. Questo spazio perso può sempre essere recuperato tramite una deframmentazione non in linea del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>Richiede che l'istanza venga arrestata anche se è attualmente in corso un backup. In genere, un backup in sospeso provocherebbe un errore di <a href="gg269298(v=exchg.10).md">JetTerm</a> con JET_errBackupInProgress. Se questo parametro non è presente, il relativo valore si presume che sia JET_bitTermAbrupt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>Richiede che l'istanza venga arrestata con tutti i database collegati rimasti in uno stato modificato.</p>
<p>Windows 7: JET_bitTermDirty è stato introdotto in Windows 7.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di backup sull'istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto. Questo errore viene restituito da <a href="gg269298(v=exchg.10).md">JetTerm</a> quando il motore è in modalità a istanze diverse e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>Impossibile arrestare l'istanza perché attualmente sono presenti sessioni con transazioni attive per l'istanza specificata. Questo errore si verifica solo se viene utilizzata la JET_bitTermComplete.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata. L'handle dell'istanza verrà inoltre chiuso e reso non disponibile a qualsiasi API che accetta un handle di istanza. Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni. Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.

Se questa funzione ha esito negativo a causa di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non vengono apportate modifiche. In caso contrario, l'istanza viene ancora arrestata come indicato per il caso di esito positivo. La differenza consiste nel fatto che l'istanza dovrà eseguire il ripristino di arresto anomalo del sistema alla successiva inizializzazione. Il motore tenterà di scaricare quanti più dati possibile per ridurre al minimo la quantità di ripristino richiesta. A livello concettuale, questo errore di [JetTerm](./jetterm-function.md) non è diverso da un arresto anomalo del processo.

#### <a name="remarks"></a>Commenti

Vedere [JetTerm](./jetterm-function.md).

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

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
