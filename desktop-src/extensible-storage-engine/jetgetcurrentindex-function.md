---
description: Altre informazioni sulla funzione JetGetCurrentIndex
title: Funzione JetGetCurrentIndex
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82f24afb4d8e36d95d6e3be480f32358c1c5dba2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468308"
---
# <a name="jetgetcurrentindex-function"></a>Funzione JetGetCurrentIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>Funzione JetGetCurrentIndex

La **funzione JetGetCurrentIndex** determina il nome dell'indice corrente di un determinato cursore. Questo nome viene usato anche per selezionare nuovamente l'indice come indice corrente usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Può anche essere usato per individuare le proprietà dell'indice usando [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*szIndexName*

Buffer di output che riceve il nome dell'indice corrente del cursore.

*cchIndexName*

Dimensione massima in caratteri del buffer di output.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intero nome dell'indice.</p><p>Il buffer di output è stato riempito con la quantità di nome dell'indice adatta. Se la lunghezza del buffer di output è di almeno un carattere, la stringa nel buffer di output sarà con terminazione Null.</p><p><strong>Nota:  </strong> Questo errore non verrà restituito se cchIndexName è zero. Per altre informazioni, vedere la sezione Osservazioni.</p> | 



In caso di esito positivo, il nome dell'indice corrente del cursore specificato verrà restituito nel buffer di output. Se JET_wrnBufferTruncated restituito, il buffer di output conterrà la quantità di nome dell'indice che si adatterà allo spazio fornito. Se la lunghezza del buffer di output è di almeno un carattere, la stringa restituita in tale buffer sarà con terminazione Null. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, lo stato del buffer di output non sarà definito. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se non è presente alcun indice corrente per il cursore, verrà restituita una stringa vuota. Ciò può verificarsi quando il cursore si trova sull'indice cluster della tabella e non è stato definito alcun indice primario. Questo indice è noto come indice sequenziale della tabella e non ha alcuna definizione. In ogni caso, l'impostazione dell'indice corrente su una stringa vuota tramite [JetSetCurrentIndex](./jetsetcurrentindex-function.md) selezionerà l'indice cluster indipendentemente dalla presenza di una definizione di indice primario.

In questa funzione è presente un bug importante in tutte le versioni. Se il buffer di output è troppo piccolo per ricevere l'intero nome dell'indice e la lunghezza del buffer di output è di almeno un carattere, JET_wrnBufferTruncated non verrà restituito. JET_errSuccess verrà restituito . Per evitare questo problema, il buffer di output deve avere sempre una lunghezza di almeno JET_cbNameMost + 1 (65).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
