---
description: Altre informazioni sulla funzione JetGotoSecondaryIndexBookmark
title: Funzione JetGotoSecondaryIndexBookmark
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca8b05c0eeac88521d03b95a94f7d2363d5746e9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468948"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Funzione JetGotoSecondaryIndexBookmark


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>Funzione JetGotoSecondaryIndexBookmark

La **funzione JetGotoSecondaryIndexBookmark** posiziona un cursore su una voce di indice associata al segnalibro dell'indice secondario specificato. Il segnalibro dell'indice secondario deve essere usato con lo stesso indice sulla stessa tabella da cui è stato recuperato in origine. Il segnalibro di indice secondario per una voce di indice può essere recuperato **usando JetGotoSecondaryIndexBookmark**.

**Windows XP:****JetGotoSecondaryIndexBookmark** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvSecondaryKey*

Buffer contenente la chiave secondaria da utilizzare per posizionare il cursore.

*cbSecondaryKey*

Dimensione della chiave secondaria nel buffer.

*pvPrimaryBookmark*

Buffer contenente il segnalibro di chiave primaria da utilizzare per posizionare il cursore.

*cbPrimaryBookmark*

Dimensione del segnalibro della chiave primaria nel buffer.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>Nel caso in cui non sia più possibile trovare la voce di indice, il cursore verrà posizionato a sinistra nel punto in cui è stata trovata in precedenza la voce di indice. L'operazione avrà comunque esito negativo con JET_errRecordDeleted; Sarà tuttavia possibile passare alla voce di indice successiva o precedente rispetto alla voce di indice mancante.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>Il segnalibro dell'indice secondario fornito non è valido. Questo errore potrebbe essere stato generato perché la chiave secondaria è zero o il puntatore al buffer della chiave secondaria è <strong>NULL.</strong> Questo errore si verifica perché</p><ul><li><p>L'indice secondario corrente non ha un vincolo di univocità e le dimensioni del segnalibro specificato sono pari a zero.</p></li><li><p>Il puntatore del buffer del segnalibro è <strong>NULL.</strong></p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>Il cursore non si trova attualmente in un indice secondario. Non è significativo passare a un segnalibro di indice secondario quando il cursore non usa attualmente un indice secondario. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve essere usato quando il cursore non si trova in un indice secondario.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Impossibile trovare la voce di indice associata al segnalibro dell'indice secondario.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice associata al segnalibro dell'indice secondario specificato. Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo verrà annullato. Se è stata creata una chiave di ricerca per l'uso da parte del cursore, tale chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimane invariata, a meno JET_errRecordDeleted non venga restituito JET_bitBookmarkPermitVirtualCurrency specificato. In tal caso, il cursore verrà posizionato in corrispondenza della voce di indice associata al segnalibro dell'indice secondario specificato. Il cursore può essere spostato rispetto a tale posizione, ma non si trova ancora in una voce di indice valida.

Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo verrà annullato. Se è stata creata una chiave di ricerca per l'uso da parte del cursore, tale chiave di ricerca verrà eliminata. In ogni caso, non verrà apportata alcuna modifica allo stato del database.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
