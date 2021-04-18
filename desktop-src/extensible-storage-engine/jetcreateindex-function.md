---
description: 'Altre informazioni su: funzione JetCreateIndex'
title: Funzione JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313104"
---
# <a name="jetcreateindex-function"></a>Funzione JetCreateIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>Funzione JetCreateIndex

La funzione **JetCreateIndex** consente di creare un indice di dati in un database Extensible Storage Engine (ESE), che è possibile utilizzare per individuare rapidamente dati specifici.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per una particolare chiamata API.

*TableID*

Tabella per la quale verrà creato un indice.

*szIndexName*

Puntatore a una stringa con terminazione null che specifica il nome dell'indice da creare.

Il nome dell'indice deve essere conforme alle linee guida seguenti:

  - Deve contenere un numero di caratteri inferiore a JET_cbNameMost, escluso il carattere di terminazione null.

  - Deve contenere solo i caratteri delle seguenti categorie: da 0 a 9, da A A Z, da a a z e da tutti i caratteri di punteggiatura, ad eccezione di " \! " (punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero i caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.

  - Non deve iniziare con uno spazio.

  - Deve contenere almeno un carattere diverso dallo spazio.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per una particolare chiamata. Questo parametro può includere zero o più opzioni disponibili nella struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*szKey*

Puntatore a una doppia stringa con terminazione null di token delimitati da null.

Per ulteriori informazioni su questo parametro, vedere la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*cbKey*

Lunghezza, in byte, del parametro *szKey* , inclusi i due caratteri null di terminazione.

*lDensity*

Densità percentuale dell'albero iniziale B + dell'indice.

Per ulteriori informazioni su questo parametro, vedere la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
</tbody>
</table>


Per un elenco di altri errori che possono essere restituiti dalla funzione **JetCreateIndex** , vedere [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Commenti

La chiamata alla funzione **JetCreateIndex** è identica alla chiamata della funzione [JetCreateIndex2](./jetcreateindex2-function.md) con una struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenente le stesse impostazioni dei parametri di **JetCreateIndex** e un parametro *cIndexCreate* uguale a 1. Per i campi della struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) che non dispongono di parametri corrispondenti in **JetCreateIndex**, viene utilizzato un valore pari a 0.

Si noti che **JetCreateIndex** è stato sostituito da [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p>Intestazione</p></td>
<td><p>Viene dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Libreria</p></td>
<td><p>USA ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Viene implementato come <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
