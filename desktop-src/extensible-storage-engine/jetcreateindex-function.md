---
description: 'Altre informazioni su: Funzione JetCreateIndex'
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
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478397"
---
# <a name="jetcreateindex-function"></a>Funzione JetCreateIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>Funzione JetCreateIndex

La **funzione JetCreateIndex** consente di creare un indice di dati in un database ESE (Extensible Archiviazione Engine), che è possibile usare per individuare rapidamente dati specifici.

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

*tableid*

Tabella per cui verrà creato un indice.

*szIndexName*

Puntatore a una stringa con terminazione Null che specifica il nome dell'indice da creare.

Il nome dell'indice deve essere conforme alle linee guida seguenti:

  - Deve contenere meno caratteri rispetto JET_cbNameMost, senza includere il carattere null di terminazione.

  - Deve contenere solo caratteri delle categorie seguenti: da 0 a 9, da A a Z, da a a z e tutti i caratteri di punteggiatura ad eccezione di " \! " (punto esclamativo), "," (virgola), " " (parentesi quadra di apertura) e " " (parentesi quadra di chiusura), ovvero i caratteri ASCII 0x20, da 0x22 a 0x2d, da 0x2f a 0x5a, 0x5c e \[ 0x5d fino a \] 0x7f.

  - Non deve iniziare con uno spazio.

  - Deve contenere almeno un carattere diverso da uno spazio.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per una chiamata specifica. Questo parametro può includere zero o più opzioni disponibili nella [JET_INDEXCREATE](./jet-indexcreate-structure.md) struttura .

*szKey*

Puntatore a una stringa con terminazione Null doppia di token delimitati da Null.

Per altre informazioni su questo parametro, vedere la [JET_INDEXCREATE](./jet-indexcreate-structure.md) struttura .

*cbKey*

Lunghezza, in byte, del *parametro szKey,* inclusi i due caratteri Null di terminazione.

*lDensity*

Densità percentuale dell'albero B+ dell'indice iniziale.

Per altre informazioni su questo parametro, vedere la [JET_INDEXCREATE](./jet-indexcreate-structure.md) struttura .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Significato</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 



Per un elenco di errori aggiuntivi che possono essere restituiti dalla **funzione JetCreateIndex,** vedere [JetCreateIndex2.](./jetcreateindex2-function.md)

#### <a name="remarks"></a>Commenti

La chiamata della funzione **JetCreateIndex** è identica alla chiamata della funzione [JetCreateIndex2](./jetcreateindex2-function.md) con una struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenente le stesse impostazioni dei parametri di **JetCreateIndex** e un parametro *cIndexCreate* uguale a 1. Per i campi della [JET_INDEXCREATE](./jet-indexcreate-structure.md) che non hanno parametri corrispondenti in **JetCreateIndex**, viene utilizzato il valore 0.

Si noti **che JetCreateIndex** è stato sostituito da [JetCreateIndex2.](./jetcreateindex2-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p>Client</p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p>Server</p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p>Intestazione</p> | <p>Viene dichiarato in Esent.h.</p> | | <p>Libreria</p> | <p>Usa ESENT.lib.</p> | | <p>DLL</p> | <p>Richiede ESENT.dll.</p> | | <p>Unicode</p> | <p>Viene implementato come <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
