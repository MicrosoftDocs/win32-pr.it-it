---
description: Altre informazioni sulla funzione JetOpenDatabase
title: Funzione JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fc7f484921dab0967ea991ac4060e5af7d78ec0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988495"
---
# <a name="jetopendatabase-function"></a>Funzione JetOpenDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetopendatabase-function"></a>Funzione JetOpenDatabase

La **funzione JetOpenDatabase** apre un database collegato in precedenza, usando le funzioni [JetAttachDatabase](./jetattachdatabase-function.md) o [JetAttachDatabase2,](./jetattachdatabase2-function.md) da usare con una sessione di database. Questa funzione può essere chiamata più volte per lo stesso database.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da aprire.

*szConnect*

Riservato. Impostata su NULL.

*pdbid*

Puntatore a un buffer che, in caso di chiamata riuscita, contiene l'identificatore del database. Se la chiamata non riesce, il valore non è definito.

*grbit*

Gruppo di bit che specificano zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDbExclusive</p> | <p>Consente a una sola sessione di collegare un database. In genere, più sessioni possono aprire un database.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impedisce modifiche al database.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>È stato richiesto l'accesso esclusivo, ma non è stato possibile concedere l'accesso.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>È stato specificato un percorso non valido in <em>szFilename</em>. <em>szFilename deve</em> essere diverso da NULL e fare riferimento a un file valido.</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase).</a></p> | 
| <p>JET_errInvalidDatabase</p> | <p>Si è tentato di aprire un file che non è un file di database valido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Si è tentato di aprire più di un database ed è <a href="gg269337(v=exchg.10).md">stato JET_paramOneDatabasePerSession</a> stato impostato. Per altre informazioni, vedere <a href="gg294139(v=exchg.10).md">Parametri di sistema.</a></p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>Il file è stato collegato in sola lettura, ma <strong>JetOpenDatabase</strong> non ha passato JET_bitDbReadOnly. Il database è ancora aperto con accesso in sola lettura.</p> | 



#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOpenDatabaseW</strong> (Unicode) e <strong>JetOpenDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
