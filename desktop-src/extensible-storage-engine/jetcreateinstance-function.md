---
description: Altre informazioni sulla funzione JetCreateInstance
title: Funzione JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f22c411dd68b29b0cf305888f9dcce16add9a2dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985044"
---
# <a name="jetcreateinstance-function"></a>Funzione JetCreateInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>Funzione JetCreateInstance

La **funzione JetCreateInstance** alloca una nuova istanza del motore di database per l'uso in un singolo processo.

**Windows XP: JetCreateInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Buffer di output che riceve l'istanza appena creata.

*szInstanceName*

Identificatore di stringa univoco per l'istanza da creare. Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.

**Nota:** Un valore NULL viene considerato come un identificatore di stringa valido per un'istanza di . Solo un'istanza può avere un identificatore di stringa NULL.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>Il nome dell'istanza specificato è già in uso per questo processo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Questo problema può verificarsi <strong>per JetCreateInstance</strong> quando <em>pinstance</em> è <strong>NULL.</strong></p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>L'operazione non è riuscita perché non può essere usata quando il motore di database funziona in modalità a istanza singola (Windows modalità di compatibilità 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>Impossibile creare una nuova istanza perché è stato raggiunto il numero massimo di istanze. Il numero massimo di istanze supportate viene configurato tramite <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <em>usando JET_paramMaxInstances</em>.</p> | 



In caso di esito positivo, verrà allocata una nuova istanza e verrà restituito l'identificatore per l'istanza. A questo punto, tutti i parametri di sistema per l'istanza avranno i valori dei parametri di sistema predefiniti globali. Una volta allocata, un'istanza deve essere terminata e/o liberata in un secondo momento.

In caso di errore, verrà restituito un errore che rappresenta la causa dell'errore e non verrà allocata alcuna istanza.

#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a [JetInit](./jetinit-function.md) prima di poter essere usata da un oggetto diverso da [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md). Il numero massimo di istanze che possono essere create contemporaneamente è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato da una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file di checkpoint e i file di log delle transazioni.

Se la funzione ha esito positivo, il motore di database verrà automaticamente modificato in modalità a più istanze come effetto collaterale di questa chiamata. Se l'applicazione vuole consentire una sola istanza nel processo, è necessario usare [JetInit](./jetinit-function.md) per avviare il motore di database in modalità di compatibilità Windows 2000.

Se presente, *szDisplayName* verrà usato per identificare l'istanza in posizioni come registro eventi o verso altri chiamanti come applicazioni di backup (tramite funzioni come [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze).](./jetossnapshotfreeze-function.md) Se il nome visualizzato non viene specificato, verrà usato il valore *szInstanceName* univoco, se presente, in caso contrario verrà restituita una stringa vuota. Se al motore non è stata impostata la modalità di esecuzione, dopo questa chiamata verrà impostata la modalità a istanze multipla.

La tipica sequenza di avvio per un processo che potenzialmente esegue più istanze di Jet è la seguente:

  - Chiamata a [JetCreateInstance2](./jetcreateinstance2-function.md) che alloca e denomi l'istanza.

  - Più chiamate a [JetSetSystemParameter per](./jetsetsystemparameter-function.md) tale istanza per impostare parametri di sistema diversi. Si noti che alcuni parametri di sistema devono essere univoci per ogni istanza ,ad esempio [JET_paramSystemPath](./transaction-log-parameters.md) [o JET_paramLogFilePath](./transaction-log-parameters.md)), quindi molto probabilmente sarà necessario impostare ognuno di essi.

  - Avviare l'istanza [usando JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md). Per terminare e/o liberare un'istanza, è necessario [usare JetTerm](./jetterm-function.md), [JetTerm2.](./jetterm2-function.md)

Se si tratta della prima istanza da iniziare, durante questa chiamata verranno eseguiti diversi passaggi aggiuntivi per eseguire l'inizializzazione e la configurazione di base del sistema. Alcuni di questi passaggi potrebbero causare errori specifici a partire da JET_errOutOfMemory ma anche altri (vedere gli errori precedenti).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
