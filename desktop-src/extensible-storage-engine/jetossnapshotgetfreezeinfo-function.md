---
description: 'Altre informazioni su: Funzione JetOSSnapshotGetFreezeInfo'
title: Funzione JetOSSnapshotGetFreezeInfo
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e737d6fe31dde43eeba7526e740ec096db20abc9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466208"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>Funzione JetOSSnapshotGetFreezeInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>Funzione JetOSSnapshotGetFreezeInfo

La **funzione JetOSSnapshotGetFreezeInfo** recupera l'elenco di istanze e database che fanno parte della sessione di snapshot in qualsiasi momento.

**Windows Vista:****JetOSSnapshotGetFreezeInfo** è stato introdotto in Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot da iniziare.

*pcInstanceInfo*

Numero di istanze attualmente in esecuzione che fanno parte della sessione snapshot.

*paInstanceInfo*

Matrice di strutture , una per ogni istanza in esecuzione, che descrive l'istanza e i database che ne fanno parte.

*grbit*

Opzioni per questa chiamata. Questo parametro è riservato per usi futuri. L'unico valore valido è 0 (zero).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errOutOfMemory</p> | <p>La funzione non è riuscita a causa di una condizione di memoria insufficiente.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> è <strong>NULL.</strong></p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Non è in corso una sessione snapshot.</p> | 



Se questa funzione ha esito positivo, le informazioni sull'istanza vengono compilate correttamente e devono essere liberate in un secondo momento chiamando [JetFreeBuffer](./jetfreebuffer-function.md) con il puntatore alla matrice di informazioni sull'istanza restituita.

Se questa funzione ha esito negativo, non si verifica alcuna modifica dello stato del motore.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) e <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
