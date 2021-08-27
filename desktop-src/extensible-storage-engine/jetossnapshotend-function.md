---
description: Altre informazioni sulla funzione JetOSSnapshotEnd
title: Funzione JetOSSnapshotEnd
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984434"
---
# <a name="jetossnapshotend-function"></a>Funzione JetOSSnapshotEnd


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>Funzione JetOSSnapshotEnd

La **funzione JetOSSnapshotEnd** notifica al motore che la sessione snapshot è stata completata.

**Windows Vista:****JetOSSnapshotEnd** è stato introdotto in Windows Vista:.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>0</p> | <p>Fine della sessione snapshot completata.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>Sessione snapshot interrotta.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Una delle opzioni richieste non è valida, usata in modo non corretto o non implementata.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Una sessione snapshot è già in corso. ma questa operazione non è consentita.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La sessione snapshot ha avuto un timeout interno prima che si verifica questa chiamata. Di conseguenza, le operazioni di I/O tornano normali prima della chiamata.</p> | 



Se questa funzione ha esito positivo, verrà completata una sessione snapshot e verrà ripreso il normale comportamento del motore. Una nuova sessione snapshot può essere avviata in un secondo momento.

Se questa funzione ha esito negativo, il JET_errOSSnapshotTimeOut restituito viene restituito e la sessione di snapshot corrente termina, ma il blocco delle operazioni di I/O durante il periodo di snapshot non è stato rispettato internamente. Per tutti gli altri errori, lo stato della sessione snapshot non verrà modificato.

#### <a name="remarks"></a>Commenti

Questa funzione viene chiamata solo se [JetOSSnapshotThaw è](./jetossnapshotthaw-function.md) stato chiamato con JET_bitContinueAfterThaw.

Per eseguire la verifica dello snapshot e il troncamento del log, è necessario completare la sessione snapshot. Verranno generate voci del log eventi per i diversi passaggi dello snapshot.

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
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
