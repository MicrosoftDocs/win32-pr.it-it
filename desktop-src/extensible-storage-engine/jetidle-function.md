---
description: 'Altre informazioni su: Funzione JetIdle'
title: Funzione JetIdle
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: babe3077c01b6b2a9c1f2f55b48921582d6343bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984544"
---
# <a name="jetidle-function"></a>Funzione JetIdle


_**Si applica a:** Windows | Windows Server_

## <a name="jetidle-function"></a>Funzione JetIdle

La **funzione JetIdle** è inevasa e deve essere usata solo a scopo di test. **JetIdle può** essere usato per eseguire attività di pulizia inattive o controllare lo stato dell'archivio versioni in ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà usata per questa chiamata.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei bit seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>Attiva la pulizia dell'archivio versioni.</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>Riservato per utilizzi futuri. Se questo flag viene specificato, l'API restituirà JET_errInvalidgrbit.</p> | 
| <p>JET_bitIdleStatus</p> | <p>Restituisce JET_wrnIdleFull se l'archivio versioni è più della metà pieno.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un <em>parametro grbit</em> fornito all'API non è valido.</p> | 



Se questa funzione ha esito positivo, verrà attivata l'operazione appropriata o verrà visualizzato un codice di errore che indica la completetà dell'archivio versioni in base al *grbit* fornito.

Se questa funzione ha esito negativo, l'operazione richiesta non sarà stata completata correttamente.

#### <a name="remarks"></a>Commenti

L'archivio versioni mantiene il meccanismo di isolamento dello snapshot di ESE. Se l'archivio versioni è più della metà pieno, il programma potrebbe chiudere le transazioni a esecuzione lunga. Se una transazione a esecuzione lunga esaurirà l'archivio versioni, ESE interromperà l'esecuzione delle operazioni di scrittura nel database.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
