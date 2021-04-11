---
description: 'Altre informazioni su: funzione JetGetErrorInfoW'
title: JetGetErrorInfoW (funzione)
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
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132435"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW (funzione)

Funzione **JetGetErrorInfoW** BAS_ del motore di database.

Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile. Queste informazioni sono soggette a modifiche.

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

Il contesto o il valore di errore per il quale sono necessarie le informazioni estese sull'errore. Il valore passato dipende dal valore del parametro *InfoLevel* .

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo di buffer dipende dal valore del parametro *InfoLevel* . Il chiamante deve essere configurato per allineare il buffer in modo appropriato.

*cbMax*

Dimensione massima della struttura *pvResult* passata.

*InfoLevel*

Il tipo di informazioni che verranno recuperate per il contesto o le informazioni sull'errore viene specificato dal parametro *pvContext* . Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.

Nella tabella seguente sono elencati i valori possibili per questo parametro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>pvContext</em> viene interpretato come un codice di/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>pvResult</em> viene interpretato come <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>e i campi della struttura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> vengono compilati in modo appropriato.</p></td>
</tr>
</tbody>
</table>


*grbit*

Riservato.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./extensible-storage-engine-error-codes.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa situazione può verificarsi per <strong>JetGetErrorInfo</strong> quando si verifica quanto segue:</p>
<ul>
<li><p>Il valore del parametro <em>InfoLevel</em> specificato non è valido.</p></li>
<li><p>Il valore <em>grbit</em> specificato non è valido.</p></li>
<li><p>Il valore <em>cbMax</em> del buffer del parametro <em>pvResult</em> specificato è inferiore alla dimensione richiesta per l'output del parametro <em>InfoLevel</em> .</p></li>
<li><p>Per <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, il valore <a href="gg294092(v=exchg.10).md">JET_ERR</a> passato è sconosciuto al motore.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Se questo SKU di Windows non supporta questa funzione, viene restituito questo errore.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il buffer di output appropriato per il valore o il contesto di errore richiesto verrà impostato sulle informazioni di errore estese richieste.

In caso di errore, lo stato dei buffer di output sarà indefinito.

### <a name="remarks"></a>Commenti

La funzione [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e [JET_ERRCAT](./jet-errcat.md) gruppo di costanti contengono la documentazione sulle informazioni estese sugli errori restituite per *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Nota: viene implementato solo <strong>JetGetErrorInfoW</strong> (Unicode). Questa API non ha una versione (ANSI).</p></td>
</tr>
</tbody>
</table>
