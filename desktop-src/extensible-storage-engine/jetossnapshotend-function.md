---
description: 'Altre informazioni su: funzione JetOSSnapshotEnd'
title: JetOSSnapshotEnd (funzione)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128170"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd (funzione)

La funzione **JetOSSnapshotEnd** notifica al motore che la sessione snapshot è stata completata.

**Windows Vista:**  **JetOSSnapshotEnd** è stato introdotto in Windows Vista:.

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.

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
<td><p>0</p></td>
<td><p>Fine corretta della sessione snapshot.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitAbortSnapshot</p></td>
<td><p>La sessione snapshot è stata interrotta.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>Una delle opzioni richieste non è valida, viene usata in modo errato o non è stata implementata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Una sessione snapshot è già in corso. ma questa operazione non è consentita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Identificatore per la sessione snapshot non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>Il timeout della sessione snapshot è stato interno prima della chiamata. Di conseguenza, le operazioni di i/o restituite al normale prima che questa chiamata venisse eseguita.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, verrà completata una sessione snapshot e verrà ripreso il normale comportamento del motore. Una nuova sessione snapshot può essere avviata in un secondo momento.

Se questa funzione ha esito negativo, il codice restituito JET_errOSSnapshotTimeOut restituisce e la sessione snapshot corrente termina, ma il blocco di IOs durante il periodo dello snapshot non è stato rispettato internamente. Per tutti gli altri errori lo stato della sessione snapshot non verrà modificato.

#### <a name="remarks"></a>Commenti

Questa funzione viene chiamata solo se [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) è stato chiamato con JET_bitContinueAfterThaw.

Per eseguire la verifica dello snapshot e il troncamento del log, è necessario completare la sessione snapshot. Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.

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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
