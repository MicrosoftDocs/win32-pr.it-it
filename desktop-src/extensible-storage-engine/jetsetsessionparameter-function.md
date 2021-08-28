---
description: Altre informazioni sulla funzione JetSetSessionParameter
title: Funzione JetSetSessionParameter
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9451844edc9f55bda75e5ec80e4958b3c474c919
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476357"
---
# <a name="jetsetsessionparameter-function"></a>Funzione JetSetSessionParameter


_**Si applica a:** Windows | Windows Server_

La **funzione JetSetSessionParameter** configura il motore di database.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parametri

*sesid*

Specifica la sessione da utilizzare per questa chiamata.

Se specificato, l'istanza specificata viene ignorata e verrà utilizzata l'istanza associata alla sessione.

*sesparamid*

ID del parametro di sessione da impostare.

*pvParam*

Dati da impostare in questo parametro di sessione.

*cbParam*

Dimensioni dei dati forniti.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L'istanza è stata inizializzata tramite una chiamata alla <a href="gg294068(v=exchg.10).md">funzione JetInit</a> e questa operazione non può essere eseguita di conseguenza. Ciò può verificarsi quando si tenta di configurare un parametro di sistema dopo che una modifica al valore del parametro non può più influire sullo stato del motore di database.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>I parametri dell'indice di tupla specificati non sono validi. Questo errore viene restituito solo <em>quando il JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o JET_paramIndexTuplesToIndexMax <em>parametro</em> è impostato su un valore non valido. Per informazioni su questi parametri, vedere <a href="gg294119(v=exchg.10).md">Parametri di indice.</a></p> | 
| <p>JET_errInitInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa situazione può verificarsi quando si verifica quanto segue:</p><ul><li><p>L'ID del parametro di sistema specificato non è valido o non è supportato.</p></li><li><p>Si è tentato di impostare un parametro di sistema con valori stringa con una stringa la cui lunghezza non rientra nell'intervallo valido per il parametro.</p></li><li><p>Si è tentato di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della relativa rappresentazione del percorso assoluto non rientra nell'intervallo valido per tale parametro.</p></li><li><p>Si è tentato di impostare un parametro di sistema con valori interi con un numero intero non compreso nell'intervallo valido per il parametro.</p></li><li><p>Si è tentato di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Null, un LCID non valido o un set non supportato di flag <strong>LCMapString.</strong></p></li><li><p>Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</p></li><li><p>È stato effettuato un tentativo di impostare un parametro di sistema dopo la chiamata della funzione <a href="gg294068(v=exchg.10).md">JetInit,</a> il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</p></li><li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per tale parametro di sistema.</p></li><li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per tale parametro di sistema.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Il percorso file system specificato non è valido. Questo errore può essere restituito da <strong>JetSetSessionParameter solo quando si</strong> impostano parametri di sistema che rappresentano file system percorsi. Ad esempio, il <em>parametro JET_paramSystemPath</em> può restituire questo errore. Per informazioni su questo parametro, vedere <a href="gg269235(v=exchg.10).md">Parametri del log delle transazioni.</a></p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p><p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p> | 
| <p>JET_errInvalidInstance</p> | <p>L'handle di istanza non è valido o fa riferimento a un'istanza che è stata arrestata.</p><p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p> | 



In caso di esito positivo, il parametro di sistema verrà impostato sul valore specificato.

In caso di errore, il valore del parametro di sistema rimarrà invariato.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
