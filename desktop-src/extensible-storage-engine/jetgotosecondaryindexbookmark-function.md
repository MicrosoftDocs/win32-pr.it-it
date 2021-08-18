---
description: Altre informazioni sulla funzione JetGotoSecondaryIndexBookmark
title: Funzione JetGotoSecondaryIndexBookmark
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e720286c3e7308078d5d5ec91aa27edc95b725830824473e7b5858f2de5bc90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072479"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Funzione JetGotoSecondaryIndexBookmark


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>Funzione JetGotoSecondaryIndexBookmark

La **funzione JetGotoSecondaryIndexBookmark** posiziona un cursore su una voce di indice associata al segnalibro dell'indice secondario specificato. Il segnalibro dell'indice secondario deve essere usato con lo stesso indice sulla stessa tabella da cui è stato recuperato in origine. Il segnalibro di indice secondario per una voce di indice può essere recuperato **usando JetGotoSecondaryIndexBookmark**.

**Windows XP:****JetGotoSecondaryIndexBookmark** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvSecondaryKey*

Buffer contenente la chiave secondaria da utilizzare per posizionare il cursore.

*cbSecondaryKey*

Dimensione della chiave secondaria nel buffer.

*pvPrimaryBookmark*

Buffer contenente il segnalibro di chiave primaria da utilizzare per posizionare il cursore.

*cbPrimaryBookmark*

Dimensione del segnalibro della chiave primaria nel buffer.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>Nel caso in cui non sia più possibile trovare la voce di indice, il cursore verrà posizionato a sinistra nel punto in cui è stata trovata in precedenza la voce di indice. L'operazione avrà comunque esito negativo con JET_errRecordDeleted; Sarà tuttavia possibile passare alla voce di indice successiva o precedente rispetto alla voce di indice mancante.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Il segnalibro dell'indice secondario fornito non è valido. Questo errore potrebbe essere stato generato perché la chiave secondaria è zero o il puntatore al buffer della chiave secondaria è <strong>NULL.</strong> Questo errore si verifica perché</p>
<ul>
<li><p>L'indice secondario corrente non ha un vincolo di univocità e le dimensioni del segnalibro specificato sono pari a zero.</p></li>
<li><p>Il puntatore del buffer del segnalibro è <strong>NULL.</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Il cursore non si trova attualmente in un indice secondario. Non è significativo passare a un segnalibro di indice secondario quando il cursore non usa attualmente un indice secondario. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve essere usato quando il cursore non si trova in un indice secondario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Impossibile trovare la voce di indice associata al segnalibro dell'indice secondario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice associata al segnalibro dell'indice secondario specificato. Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo verrà annullato. Se è stata costruita una chiave di ricerca per l'uso da parte del cursore, tale chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimane invariata, a meno JET_errRecordDeleted non venga restituito JET_bitBookmarkPermitVirtualCurrency specificato. In tal caso, il cursore verrà posizionato in corrispondenza della voce di indice associata al segnalibro dell'indice secondario specificato. Il cursore può essere spostato rispetto a tale posizione, ma non si trova ancora in una voce di indice valida.

Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo verrà annullato. Se è stata costruita una chiave di ricerca per l'uso da parte del cursore, tale chiave di ricerca verrà eliminata. In ogni caso, non verrà apportata alcuna modifica allo stato del database.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
