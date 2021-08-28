---
description: Altre informazioni sulla funzione JetGetErrorInfoW
title: Funzione JetGetErrorInfoW
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f459d98ee2cc3c0bb1b57eb5cd4fb630d076836b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468978"
---
# <a name="jetgeterrorinfow-function"></a>Funzione JetGetErrorInfoW


_**Si applica a:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>Funzione JetGetErrorInfoW

Funzione **JetGetErrorInfoW** BAS_ del motore di database.

Nota: questa documentazione è basata su una versione preliminare di Extensible Archiviazione Engine. Queste informazioni sono soggette a modifiche.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parametri

*pvContext*

Contesto o valore di errore per il quale sono necessarie le informazioni sull'errore esteso. Il valore passato dipende dal valore *del parametro InfoLevel.*

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo del buffer dipende dal valore *del parametro InfoLevel.* Il chiamante deve essere configurato per allineare il buffer in modo appropriato.

*cbMax*

Dimensione massima della *struttura pvResult* passata.

*InfoLevel*

Il tipo di informazioni che verranno recuperate per le informazioni sull'errore/contesto viene specificato dal *parametro pvContext.* Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel.*

Nella tabella seguente sono elencati i valori possibili per questo parametro.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvContext</em> viene interpretato come <a href="gg269297(v=exchg.10).md">codice JET_ERR</a>/error, <em>pvResult</em> viene interpretato come <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>e i campi della struttura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> vengono compilati in modo appropriato.</p> | 



*grbit*

Riservato.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./extensible-storage-engine-error-codes.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Ciò può verificarsi <strong>per JetGetErrorInfo</strong> quando si verifica quanto segue:</p><ul><li><p>Il valore <em>del parametro InfoLevel</em> specificato non è valido.</p></li><li><p>Il valore <em>grbit specificato</em> non è valido.</p></li><li><p>Il valore <em>cbMax</em> del buffer del parametro <em>pvResult</em> specificato è minore delle dimensioni richieste per l'output di <em>questo parametro InfoLevel.</em></p></li><li><p>Per <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, <a href="gg294092(v=exchg.10).md">il</a> valore JET_ERR passato è sconosciuto al motore.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Se questo SKU di windows non supporta questa funzione, verrà restituito questo errore.</p> | 



In caso di esito positivo, il buffer di output appropriato per il contesto/valore di errore richiesto verrà impostato sulle informazioni sull'errore estese richieste.

In caso di errore, lo stato dei buffer di output non sarà definito.

### <a name="remarks"></a>Commenti

La [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e [il JET_ERRCAT](./jet-errcat.md) di costanti contengono la documentazione sulle informazioni sugli errori estesi restituite per *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows 8 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Nota: viene implementato <strong>solo JetGetErrorInfoW</strong> (Unicode). Questa API non ha una versione A (ANSI).</p> | 

