---
description: 'Altre informazioni su: funzione JetIdle'
title: JetIdle (funzione)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883465"
---
# <a name="jetidle-function"></a>JetIdle (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetidle-function"></a>JetIdle (funzione)

La funzione **JetIdle** è inattiva e deve essere usata solo a scopo di test. **JetIdle** può essere utilizzato per eseguire attività di pulizia inattive o controllare lo stato dell'archivio versioni in ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà utilizzata per questa chiamata.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei bit seguenti:

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
<td><p>JET_bitIdleCompact</p></td>
<td><p>Attiva la pulizia dell'archivio delle versioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIdleFlushBuffers</p></td>
<td><p>Riservato per utilizzi futuri. Se questo flag è specificato, l'API restituirà JET_errInvalidgrbit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIdleStatus</p></td>
<td><p>Restituisce JET_wrnIdleFull se l'archivio delle versioni supera la metà.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un parametro <em>grbit</em> fornito all'API non è valido.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, verrà attivata l'operazione appropriata oppure un codice di errore che indica il modo in cui l'archivio versione è pieno a seconda del *grbit* fornito.

Se questa funzione ha esito negativo, l'operazione richiesta non viene completata correttamente.

#### <a name="remarks"></a>Commenti

L'archivio versioni mantiene il meccanismo di isolamento dello snapshot di ESE. Se l'archivio delle versioni supera la metà, il programma potrebbe chiudere transazioni con esecuzione prolungata. Se una transazione con esecuzione prolungata esaurisce l'archivio versioni, ESE smetterà di consentire operazioni di scrittura nel database.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
