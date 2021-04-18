---
description: 'Altre informazioni su: Enumerazione JET_prep'
title: Enumerazione JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316478"
---
# <a name="jet_prep-enumeration"></a>Enumerazione JET_prep

Tipi di aggiornamento per JetPrepareUpdate.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Insert</td>
<td>Questo flag determina la preparazione del cursore per l'inserimento di un nuovo record. Tutti i dati vengono inizializzati sullo stato predefinito per il record. Se la tabella include una colonna con incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo o negativo.</td>
</tr>
<tr class="even">
<td></td>
<td>Sostituisci</td>
<td>Questo flag determina la preparazione del cursore per la sostituzione del record corrente. Se la tabella contiene una colonna versione, la colonna Version viene impostata sul valore successivo nella sequenza. Se l'aggiornamento non viene completato, il valore della versione nel record non sarà interessato. Viene assunto un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare questo record prima del completamento della sessione.</td>
</tr>
<tr class="odd">
<td></td>
<td>Annulla</td>
<td>Questo flag fa in modo che JetPrepareUpdate annulli l'aggiornamento per questo cursore.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Questo flag è simile a JET_prepReplace, ma non viene effettuato alcun blocco per impedire ad altre sessioni di aggiornare questo record. Questa sessione può invece ricevere JET_errWriteConflict quando chiama JetUpdate per completare l'aggiornamento.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Questo flag determina la preparazione del cursore per l'inserimento di una copia del record esistente. Se viene utilizzata questa opzione, deve essere presente un record corrente. Lo stato iniziale del nuovo record viene copiato dal record corrente. I valori Long archiviati in modalità non registrata vengono copiati virtualmente.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Questo flag determina la preparazione del cursore per un inserimento dello stesso record e per l'eliminazione o il record originale. Viene utilizzato nei casi in cui la chiave primaria è stata modificata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
