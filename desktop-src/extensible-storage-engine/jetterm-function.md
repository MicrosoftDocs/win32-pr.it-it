---
description: 'Altre informazioni su: funzione JetTerm'
title: Funzione JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306210"
---
# <a name="jetterm-function"></a>Funzione JetTerm


_**Si applica a:** Windows | Windows Server_

## <a name="jetterm-function"></a>Funzione JetTerm

La funzione **JetTerm** avvia l'arresto di un'istanza che è stata inizializzata da [JetInit](./jetinit-function.md).

**JetTerm** può essere utilizzato anche per eliminare un'istanza non inizializzata creata da [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Specifica l'istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **null**.

**Windows XP e versioni successive:**  Questo parametro è sovraccarico. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **null** o potrebbe contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). Se il motore funziona in modalità a istanze diverse, questo parametro deve essere un puntatore a un'istanza creata con [JetCreateInstance](./jetcreateinstance-function.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto. Questo errore viene restituito da <strong>JetTerm</strong> quando il motore è in modalità a istanze diverse e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di backup sull'istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>Impossibile arrestare l'istanza perché attualmente sono presenti sessioni con transazioni attive per l'istanza specificata. Questo errore si verifica solo se viene utilizzata la JET_bitTermComplete.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata. L'handle dell'istanza verrà inoltre chiuso e reso non disponibile a qualsiasi API che accetta un handle di istanza. Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni. Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.

Se questa funzione ha esito negativo a causa di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non vengono apportate modifiche. In caso contrario, l'istanza viene ancora arrestata in base al caso di esito positivo. La differenza consiste nel fatto che l'istanza dovrà eseguire il ripristino di arresto anomalo del sistema alla successiva inizializzazione. Il motore tenterà di scaricare quanti più dati possibile per ridurre al minimo la quantità di ripristino richiesta. A livello concettuale, questo errore di **JetTerm** non è diverso da un arresto anomalo del processo.

#### <a name="remarks"></a>Commenti

Se il processo host di un'istanza viene chiuso per qualsiasi motivo prima che **JetTerm** venga chiamato correttamente su tale istanza, l'istanza viene considerata in stato arrestato in modo anomalo. Il ripristino dell'arresto anomalo si verificherà al successivo tentativo di inizializzare l'istanza.

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
[JetTerm2](./jetterm2-function.md)
