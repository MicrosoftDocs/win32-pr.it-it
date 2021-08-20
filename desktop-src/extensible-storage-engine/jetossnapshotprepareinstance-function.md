---
description: Altre informazioni sulla funzione JetOSSnapshotPrepareInstance
title: Funzione JetOSSnapshotPrepareInstance
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfd4fc15f3ea7d4f6275f0d4dd31ed96729715b6089397fff7ee73fc7d0c6e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614936"
---
# <a name="jetossnapshotprepareinstance-function"></a>Funzione JetOSSnapshotPrepareInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>Funzione JetOSSnapshotPrepareInstance

La **funzione JetOSSnapshotPrepareInstance** seleziona un'istanza specifica come parte della sessione snapshot.

**Windows Vista:** **JetOSSnapshotPrepareInstance** è stato introdotto in Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
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

Opzioni per questa chiamata. Questo parametro è riservato per usi futuri. L'unico valore valido è 0 (zero).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>Il puntatore id snapshot è <strong>NULL</strong> o il <em>parametro grbit</em> non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Una sessione snapshot è già in corso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>L'identificatore per la sessione snapshot non è valido.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'istanza specificata farà parte della sessione snapshot.

Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.

#### <a name="remarks"></a>Commenti

La normale chiamata alla sequenza API è: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), facoltativamente seguita da una o più chiamate a **JetOSSnapshotPrepareInstance** e quindi [da JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Dopo l'avvio, il blocco può essere terminato usando [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md). Verranno generate voci del log eventi per i diversi passaggi dello snapshot.

Se **JetOSSnapshotPrepareInstance** non viene chiamato tra l'inizio della sessione ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e il momento di blocco ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), tutte le istanze in esecuzione nel motore si bloccano e diventano parte della sessione snapshot. Ciò si verifica per due motivi:

  - Semplifica il codice per gli utenti che vogliono tutte le istanze.

  - Consente la compatibilità con le versioni precedenti per i chiamanti delle API snapshot.

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
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
