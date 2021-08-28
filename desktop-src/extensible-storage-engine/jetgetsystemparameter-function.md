---
description: Altre informazioni sulla funzione JetGetSystemParameter
title: Funzione JetGetSystemParameter
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 608a9c464ca645668483934a28a3f79945cd443d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984744"
---
# <a name="jetgetsystemparameter-function"></a>Funzione JetGetSystemParameter


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetsystemparameter-function"></a>Funzione JetGetSystemParameter

La **funzione JetGetSystemParameter** legge le numerose impostazioni di configurazione del motore di database.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre **NULL.**

Per Windows XP e versioni successive, questo parametro è in qualche modo sottoposto a overload. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **NULL** o contenere l'istanza effettiva restituita da [JetInit.](./jetinit-function.md) In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da tale istanza. Se il motore funziona in modalità a istanza multipla, questo parametro può essere **NULL** o un puntatore a un'istanza creata usando [JetInit](./jetinit-function.md) o [JetCreateInstance.](./jetcreateinstance-function.md) Quando questo parametro è **NULL,** viene letta l'impostazione del parametro di sistema globale (o predefinita). Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.

*sesid*

Sessione da utilizzare per questa chiamata.

Se specificato, l'istanza specificata viene ignorata e verrà utilizzata l'istanza associata alla sessione.

*paramid*

ID del parametro di sistema che verrà letto.

Per [un elenco completo](./extensible-storage-engine-system-parameters.md) dei parametri di sistema e delle relative proprietà, vedere Parametri di sistema.

*plParam*

Buffer di output che riceve il valore del parametro di sistema selezionato se il parametro di sistema è di tipo Integer.

*szParam*

Buffer di output che riceve il valore del parametro di sistema selezionato se il parametro di sistema è di tipo stringa.

*cbMax*

Dimensione massima in byte del buffer di output della stringa.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInitInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p><p>Questa operazione può verificarsi <strong>per JetGetSystemParameter</strong> quando:</p><ul><li><p>L'ID del parametro di sistema specificato non è valido o non è supportato.</p></li><li><p>Il parametro di sistema specificato richiede che sia specificato il buffer di output integer e che il puntatore del buffer di output sia <strong>NULL.</strong></p></li><li><p>Il parametro di sistema specificato richiede che sia specificato un buffer di output di stringa e che il puntatore del buffer di output sia <strong>NULL.</strong></p><p><strong>Windows Vista:</strong> Questa operazione può verificarsi solo Windows Vista e versioni successive.</p></li><li><p>Il parametro di sistema specificato richiede che venga fornito un buffer di output di stringa e che le dimensioni del buffer di output siano troppo piccole per accettare una stringa con terminazione Null.</p><p><strong>Windows Vista:</strong> Questa operazione può verificarsi solo Windows Vista e versioni successive.</p></li><li><p>Impossibile leggere il parametro di sistema specificato perché è di sola scrittura.</p></li><li><p>Il parametro di sistema specificato è solo globale e si è tentato di leggere un valore specifico dell'istanza per tale parametro di sistema. Questa operazione può verificarsi solo in Windows XP e versioni successive.</p></li><li><p>Il parametro di sistema specificato è solo per istanza e si è tentato di leggere il valore globale per tale parametro di sistema. Questa operazione può verificarsi solo in Windows XP e versioni successive.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p> | 
| <p>JET_errInvalidInstance</p> | <p>L'handle di istanza non è valido o fa riferimento a un'istanza di che è stata arrestato. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p><p><strong>Windows Vista:</strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L'operazione è stata completata correttamente, ma il buffer di output è troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</p><p>Il buffer di output è stato riempito con l'impostazione del parametro di sistema corrispondente. Se la lunghezza del buffer di output è di almeno un carattere, la stringa in tale buffer di output avrà terminazione Null.</p><p><strong>Nota  </strong> Questo errore non viene restituito da tutte le versioni. Per altre informazioni, vedere la sezione Osservazioni.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L'operazione non è riuscita perché il buffer di output è troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</p><p><strong>Nota  </strong> Questo errore non viene restituito in alcuni casi per mantenere la compatibilità dell'applicazione. Per altre informazioni, vedere la sezione Osservazioni.</p><p><strong>Windows Vista:</strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</p> | 



In caso di esito positivo, il buffer di output appropriato per il parametro di sistema richiesto verrà impostato sul valore di tale parametro di sistema.

In caso di errore, lo stato dei buffer di output non sarà definito.

#### <a name="remarks"></a>Commenti

Esiste un problema importante in questa API presente in tutte le versioni. Se viene richiesto un parametro di sistema con un valore stringa e il buffer di output è troppo piccolo per ricevere l'intera impostazione del parametro di sistema, JET_wrnBufferTruncated non verrà restituito. JET_errSuccess viene invece restituito . Se la lunghezza della stringa restituita è uguale alla dimensione del buffer di output meno il terminatore **NULL,** il chiamante deve reagire come se JET_wrnBufferTruncated restituito. Se viene specificato un buffer di output di stringa di dimensioni zero, il chiamante deve reagire come se JET_errInvalidParameter restituito.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
