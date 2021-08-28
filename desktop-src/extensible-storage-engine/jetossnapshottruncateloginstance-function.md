---
description: Altre informazioni sulla funzione JetOSSnapshotTruncateLogInstance
title: Funzione JetOSSnapshotTruncateLogInstance
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0986633a450052431dfcef1426488dddc0417d33
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988444"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Funzione JetOSSnapshotTruncateLogInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>Funzione JetOSSnapshotTruncateLogInstance

La **funzione JetOSSnapshotTruncateLogInstance** tronca il log per un'istanza specificata durante una sessione di snapshot.

**Windows Vista:****JetOSSnapshotTruncateLogInstance** è stato introdotto in Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*Istanza*

Istanza di che verrà utilizzata per questa chiamata.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.

*grbit* può essere uno dei valori seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Tutti i database sono collegati in modo che il motore di archiviazione possa calcolare ed eseguire il troncamento del log.</p> | 
| <p>0 (zero)</p> | <p>Non si verificherà alcun troncamento.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Il <em>parametro grbit</em> non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La sessione snapshot non è nello stato in cui può verificarsi un troncamento. Le cause possibili sono:</p><ul><li><p>La chiamata viene completata dopo il timeout della sessione snapshot.</p></li><li><p>La sessione è stata specificata come snapshot di copia.</p></li></ul> | 



Se questa funzione ha esito positivo, i file di log per una o tutte le istanze che fanno parte della sessione snapshot verranno troncati, se possibile.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata solo se lo snapshot è stato creato con l'opzione JET_bitContinueAfterThaw. In caso contrario, la sessione snapshot termina dopo la chiamata a [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
