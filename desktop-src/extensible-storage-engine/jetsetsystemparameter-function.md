---
description: Altre informazioni sulla funzione JetSetSystemParameter
title: Funzione JetSetSystemParameter
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da3dc4c0d211039378b5cc1301a84e35f67ab24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475797"
---
# <a name="jetsetsystemparameter-function"></a>Funzione JetSetSystemParameter


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>Funzione JetSetSystemParameter

La **funzione JetSetSystemParameter** viene usata per impostare le numerose impostazioni di configurazione del motore di database.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Specifica l'istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Per Windows 2000, questo parametro viene ignorato e deve sempre essere **NULL.**

**Windows XP:**  Per Windows XP e versioni successive, questo parametro è in qualche modo sottoposto a overload. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **NULL** o può contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da tale istanza. Se il motore funziona in modalità a più istanze, questo parametro può essere **NULL** o un puntatore a un'istanza creata tramite [JetInit](./jetinit-function.md) o [JetCreateIndex.](./jetcreateindex-function.md) Quando questo parametro è **NULL,** viene letta l'impostazione del parametro di sistema globale (o predefinita). Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.

Anche se si tratta tecnicamente di un parametro out, questa API non modifica mai il contenuto del buffer fornito.

*sesid*

Specifica la sessione da utilizzare per questa chiamata.

Se specificato, l'istanza specificata viene ignorata e verrà usata l'istanza associata alla sessione.

*paramid*

ID del parametro di sistema che verrà impostato. Per [un elenco completo](./extensible-storage-engine-system-parameters.md) dei parametri di sistema e delle relative proprietà, vedere Parametri di sistema.

*lParam*

Fornisce il valore da impostare per il parametro di sistema selezionato se il parametro di sistema è di tipo Integer.

*szParam*

Fornisce il valore per il parametro di sistema selezionato se il parametro di sistema è di tipo stringa.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p><p><strong>Windows Vista:</strong>  In Windows Vista e versioni successive, l'esito positivo può essere restituito senza modificare il valore del parametro di sistema. Per altre informazioni, vedere JET_paramEnableAdvanced parametro di sistema nell'argomento <a href="gg269346(v=exchg.10).md">Meta Parameters</a> .</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L'istanza è stata inizializzata usando una chiamata a <a href="gg294068(v=exchg.10).md">JetInit</a> e questa operazione non può essere eseguita di conseguenza. Ciò può verificarsi per <strong>JetSetSystemParameter</strong> quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica del relativo valore non può influire sullo stato del motore di database.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>I parametri dell'indice di tupla specificati non sono validi. Questo errore può essere restituito da <strong>JetSetSystemParameter</strong> solo quando si imposta <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può verificarsi solo Windows XP e Windows Server 2003.</p> | 
| <p>JET_errInitInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <strong>JetSetSystemParameter</strong> quando:</p><ul><li><p>L'ID del parametro di sistema specificato non è valido o non è supportato.</p></li><li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori stringa con una stringa la cui lunghezza non rientra nell'intervallo valido per il parametro.</p></li><li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della relativa rappresentazione di percorso assoluto non rientra nell'intervallo valido per tale parametro.</p><p><strong>Windows Vista:</strong>  Questo problema può verificarsi solo in Windows Vista e versioni successive.</p></li><li><p>È stato effettuato un tentativo di impostare un parametro di sistema con valori interi con un numero intero non compreso nell'intervallo valido per il parametro.</p></li><li><p>È stato effettuato un tentativo di <strong></strong>impostare JET_paramUnicodeIndexDefault con un puntatore<a href="gg294097(v=exchg.10).md">null JET_UNICODEINDEX,</a> un LCID non valido o un set non supportato di flag LCMapString.</p><p><strong>Windows Vista:</strong>  Questo problema può verificarsi solo in Windows Vista e versioni successive.</p></li><li><p>Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</p></li><li><p>È stato effettuato un tentativo di impostare un parametro di sistema dopo la chiamata a <a href="gg294068(v=exchg.10).md">JetInit,</a> il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può verificarsi solo Windows XP e Windows Server 2003.</p></li><li><p>Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per tale parametro di sistema.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può verificarsi solo Windows XP e Windows Server 2003.</p></li><li><p>Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per tale parametro di sistema.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può verificarsi solo Windows XP e Windows Server 2003.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Il percorso file system specificato non è valido. Questo errore può essere restituito da <strong>JetSetSystemParameter solo</strong> quando si impostano parametri di sistema che rappresentano file system percorsi. Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> può restituire questo errore.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p><p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p> | 
| <p>JET_errInvalidInstance</p> | <p>L'handle dell'istanza non è valido o fa riferimento a un'istanza che è stata arrestato.</p><p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p><p><strong>Windows Vista:</strong>  Questo errore verrà restituito solo da Windows Vista e versioni successive.</p> | 



In caso di esito positivo, l'impostazione per il parametro di sistema verrà impostata sul valore specificato.

In caso di errore, l'impostazione per il parametro di sistema rimarrà invariata.

#### <a name="remarks"></a>Commenti

**JetSetSystemParameter** esegue un processo non valido di convalida dell'impostazione scelta per ogni parametro di sistema. È necessario fare attenzione a non basarsi su questa convalida per applicare impostazioni buone. Prestare particolare attenzione alla descrizione di ogni parametro di sistema e seguire queste linee guida per una buona impostazione dei parametri di sistema.

È necessario impostare sempre un set di parametri di sistema per garantire che il motore di database funzioni come previsto. In particolare, tutti i parametri di sistema che influiscono sul layout fisico dei file usati dal motore di database devono sempre essere impostati. Per altre informazioni, vedere [Parametri di sistema](./extensible-storage-engine-system-parameters.md).

Ogni parametro di sistema ha un valore predefinito. Questi valori predefiniti si sono evoluti nel tempo e sono piuttosto arbitrari. È consigliabile che un'applicazione valuti tutti i valori predefiniti per assicurarsi che siano appropriati. Se non sono appropriati, devono essere configurati dall'applicazione. Questo è importante perché molti di questi parametri possono influire notevolmente sull'affidabilità, sulle prestazioni e sull'utilizzo delle risorse del motore di database.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
