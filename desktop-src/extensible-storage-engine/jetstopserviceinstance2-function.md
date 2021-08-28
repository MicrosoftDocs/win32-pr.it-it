---
description: Altre informazioni sulla funzione JetStopServiceInstance2
title: Funzione JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b5446306bd4035c68f33db2966b1cfadd0b6d82
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987234"
---
# <a name="jetstopserviceinstance2-function"></a>Funzione JetStopServiceInstance2


_**Si applica a:** Windows | Windows Server_

La **funzione JetStopServiceInstance2** prepara un'istanza prima di Suspend e prepara un'istanza dopo Resume. Sospendi e Riprendi sono stati di esecuzione del modello Windows ciclo di vita dell'app di Store.

La **funzione JetStopServiceInstance2** è stata introdotta in Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di destinazione. Il **JET_INSTANCE** di dati è un handle per l'istanza del database da usare per una chiamata all'API JET. Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2.](./jetinit2-function.md)

*grbit*

Gruppo di bit che specifica uno o più valori elencati e definiti nella tabella seguente.


| <p>Valore</p> | <p>Descrizione</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>Arresta tutti i servizi ESE (Extensible Archiviazione Engine) per l'istanza specificata.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Arresta le attività di manutenzione in background riavviabili specificate dal client ,ad esempio B+ Tree Defrag.</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Inattiva tutte le cache dirty su disco. Questo valore è asincrono e può essere annullato.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Riprende le operazioni StopService eseguite in precedenza. in altri, il servizio viene riavviato. Questo valore può essere combinato con il <em>parametro grbits</em> per riprendere servizi specifici o con JET_bitStopServiceAll per riprendere tutti i servizi arrestati in precedenza. Questo bit può essere usato solo per riprendere StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches. Se in precedenza è stato chiamato JET_bitStopServiceAll, un tentativo di usare JET_bitStopServiceResume avrà esito negativo. Se il secondo passaggio di ripresa non viene chiamato, le prestazioni dell'applicazione saranno ridotte. In questo caso il checkpoint viene mantenuto a zero.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 



#### <a name="remarks"></a>Commenti

Questa funzione consente a un'applicazione JET di spostare la cache del database in uno stato pulito o quasi pulito (con I/O del sistema operativo inattivo), in modo che se l'applicazione fosse terminata, il ripristino sarebbe rapido. Questo approccio è preferibile rispetto alla terminazione di JET chiamando le funzioni [JetTerm](./jetterm-function.md) o [JetDetachDatabase,](./jetdetachdatabase-function.md) in modo che nello scenario più comune l'applicazione non sia più pronta e in un secondo momento l'applicazione abbia l'intera cache ed è pronta per l'uso il prima possibile.

Se questa funzione ha esito positivo, prepara la cache del database per una sospensione imminente. Questa funzione accoda il lavoro a un thread di lavoro in background e torna immediatamente al chiamante. La funzione deve essere chiamata in base a PLM VisibilityNotice anziché chiamare dal gestore eventi di sospensione dell'applicazione per garantire che JET abbia tempo per scaricare i buffer dirty prima che PLM sospende/termini il processo. Internamente, JET attiva un invio immediato di manutenzione del checkpoint in caso di modifica della configurazione (aggiornamento del checkpoint o questo nuovo bit di cache inattiva). Per altre informazioni sugli eventi VisibilityNotice, vedere [Classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Questa funzione deve essere chiamata due volte. Viene chiamato dopo che l'applicazione riceve l'avviso di sospensione dal sistema operativo, ma prima che l'applicazione sia stata sospesa. Viene quindi chiamato di nuovo dopo la ripresa dell'applicazione da parte del sistema operativo. Ad esempio:

Quando viene chiamato per Sospendere: JET_ERR JET_API JetStopServiceInstance2( istanza, JET_bitStopServiceQuiesceCaches);

Alla ripresa: JET_ERR JET_API JetStopServiceInstance2( istanza, JET_bitStopServiceQuiesceCaches| JET_bitStopServiceResume );

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
