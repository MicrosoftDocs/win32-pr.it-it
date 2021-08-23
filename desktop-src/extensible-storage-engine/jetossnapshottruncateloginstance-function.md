---
description: Altre informazioni sulla funzione JetOSSnapshotTruncateLogInstance
title: Funzione JetOSSnapshotTruncateLogInstance
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35b76b8b5aa46d107129f5b5033bf958a59488abd402bfb68c8a1d4d3b555a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728131"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Funzione JetOSSnapshotTruncateLogInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>Funzione JetOSSnapshotTruncateLogInstance

La **funzione JetOSSnapshotTruncateLogInstance** tronca il log per un'istanza specificata durante una sessione di snapshot.

**Windows Vista:****JetOSSnapshotTruncateLogInstance** è stato introdotto in Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*Istanza*

Istanza di che verrà utilizzata per questa chiamata.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.

*grbit* può essere uno dei valori seguenti:

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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Tutti i database sono collegati in modo che il motore di archiviazione possa calcolare ed eseguire il troncamento del log.</p></td>
</tr>
<tr class="even">
<td><p>0 (zero)</p></td>
<td><p>Non si verificherà alcun troncamento.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di](./extensible-storage-engine-errors.md) Archiviazione estendibile e Parametri di gestione [degli errori](./error-handling-parameters.md).

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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Il <em>parametro grbit</em> non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La sessione snapshot non è nello stato in cui può verificarsi un troncamento. Le cause possibili sono:</p>
<ul>
<li><p>La chiamata viene completata dopo il timeout della sessione snapshot.</p></li>
<li><p>La sessione è stata specificata come snapshot di copia.</p></li>
</ul></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, i file di log per una o tutte le istanze che fanno parte della sessione snapshot verranno troncati, se possibile.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata solo se lo snapshot è stato creato con l'JET_bitContinueAfterThaw predefinita. In caso contrario, la sessione snapshot termina dopo la chiamata a [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
