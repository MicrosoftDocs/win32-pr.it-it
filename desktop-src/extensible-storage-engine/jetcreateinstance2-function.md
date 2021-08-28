---
description: 'Altre informazioni su: Funzione JetCreateInstance2'
title: Funzione JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cebf23486505cd0381bd8cd62024ad0bc767633
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987424"
---
# <a name="jetcreateinstance2-function"></a>Funzione JetCreateInstance2


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateinstance2-function"></a>Funzione JetCreateInstance2

La **funzione JetCreateInstance2** viene usata per allocare una nuova istanza del motore di database per l'uso in un singolo processo, con un nome visualizzato specificato.

**Windows XP:****JetCreateInstance2** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Buffer di output che riceverà l'istanza appena creata.

*szInstanceName*

Specifica un identificatore di stringa univoco per l'istanza da creare. Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.

**Nota** Un valore NULL viene considerato come un identificatore di stringa valido per un'istanza di . Solo un'istanza può avere un identificatore di stringa NULL.

*szDisplayName*

Nome visualizzato per l'istanza da creare. Quando questo parametro non è presente, si presuppone che il relativo valore sia NULL.

*grbit*

Riservato per utilizzi futuri. Quando questo parametro non è presente, si presuppone che il relativo valore sia zero.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>Il nome dell'istanza specificato è già in uso per questo processo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi <a href="gg269354(v=exchg.10).md">per JetCreateInstance</a> quando <em>pinstance</em> è NULL.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>L'operazione non è riuscita perché non può essere usata quando il motore di database funziona in modalità a istanza singola (Windows compatibilità 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>Non è stato possibile creare una nuova istanza perché è stato raggiunto il numero massimo di istanze. Il numero massimo di istanze supportate viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <em>JET_paramMaxInstances</em>.</p> | 



In caso di esito positivo, verrà allocata una nuova istanza e verrà restituito l'identificatore corrispondente. A questo punto, tutti i parametri di sistema per l'istanza avranno i valori dei parametri di sistema predefiniti globali. Una volta allocata, un'istanza deve essere terminata e/o liberata in un secondo momento.

In caso di errore, verrà restituito un errore che rappresenta la causa dell'errore e non verrà allocata alcuna istanza.

#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a [JetInit](./jetinit-function.md) prima di poter essere usata da qualsiasi elemento diverso da [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando [JetInit.](./jetinit-function.md) Il numero massimo di istanze che possono essere create contemporaneamente è controllato da *JET_paramMaxInstances*, che può essere configurato da una chiamata a [JetSetSystemParameter.](./jetsetsystemparameter-function.md) Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Se la funzione ha esito positivo, il motore di database verrà automaticamente modificato in modalità a istanza multipla come effetto collaterale di questa chiamata. Se l'applicazione vuole consentire una sola istanza nel processo, è necessario usare [JetInit](./jetinit-function.md) per avviare il motore di database in modalità di compatibilità Windows 2000.

Se presente, il *parametro szDisplayName* verrà usato per identificare l'istanza in posizioni come il registro eventi o verso altri chiamanti come le applicazioni di backup (tramite funzioni come [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze).](./jetossnapshotfreeze-function.md) Se non viene specificato il nome visualizzato, verrà usato il parametro *szInstanceName* univoco, se presente. In caso contrario, verrà restituita una stringa vuota. Se per il motore non è stata impostata la modalità di esecuzione, dopo questa chiamata verrà impostata la modalità a istanze multipla.

La sequenza di avvio tipica per un processo che potenzialmente esegue più istanze di Jet è la seguente:

  - Chiamata a **JetCreateInstance2 che** alloca e assegna un nome all'istanza.

  - Più chiamate a [JetSetSystemParameter per](./jetsetsystemparameter-function.md) tale istanza per impostare parametri di sistema diversi. Si noti che alcuni parametri di sistema devono essere univoci per ogni istanza ,ad esempio *JET_paramSystemPath* o *JET_paramLogFilePath*, quindi molto probabilmente sarà necessario impostare ognuno di questi parametri.

  - Avviare l'istanza usando [JetInit](./jetinit-function.md) o [JetInit2.](./jetinit2-function.md) Per terminare e/o liberare un'istanza, usare [JetTerm](./jetterm-function.md) o [JetTerm2.](./jetterm2-function.md)

Se questa è la prima istanza da iniziare, durante questa chiamata verranno eseguiti alcuni passaggi aggiuntivi per eseguire l'inizializzazione e la configurazione di base del sistema. Alcuni di questi passaggi potrebbero causare errori specifici a partire da JET_errOutOfMemory ma anche da altri .Per altre informazioni, vedere Valori restituiti.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateInstance2W</strong> (Unicode) e <strong>JetCreateInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
