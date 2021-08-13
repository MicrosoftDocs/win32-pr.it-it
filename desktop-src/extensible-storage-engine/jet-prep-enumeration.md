---
description: 'Altre informazioni su: Enumerazione JET_prep dati'
title: JET_prep enumerazione
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
ms.openlocfilehash: 0246114eef784fea2fc145f7cab737c815c17626fc2580b33aa6d09229418066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765055"
---
# <a name="jet_prep-enumeration"></a>JET_prep enumerazione

Tipi di aggiornamento per JetPrepareUpdate.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Questo flag fa sì che il cursore si prepari per l'inserimento di un nuovo record. Tutti i dati vengono inizializzati allo stato predefinito per il record. Se la tabella include una colonna a incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo, negativo o annullato.</td>
</tr>
<tr class="even">
<td></td>
<td>Sostituisci</td>
<td>Questo flag fa sì che il cursore si prepari per una sostituzione del record corrente. Se la tabella include una colonna versione, la colonna della versione viene impostata sul valore successivo nella relativa sequenza. Se l'aggiornamento non viene completato, il valore della versione nel record non sarà interessato. Viene utilizzato un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare il record prima del completamento della sessione.</td>
</tr>
<tr class="odd">
<td></td>
<td>Annulla</td>
<td>Questo flag fa sì che JetPrepareUpdate annulli l'aggiornamento per questo cursore.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Questo flag è simile a JET_prepReplace, ma non viene intrapreso alcun blocco per impedire ad altre sessioni di aggiornare questo record. Al contrario, questa sessione può ricevere JET_errWriteConflict quando chiama JetUpdate per completare l'aggiornamento.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Questo flag fa sì che il cursore si prepari per l'inserimento di una copia del record esistente. Se si usa questa opzione, deve essere presente un record corrente. Lo stato iniziale del nuovo record viene copiato dal record corrente. I valori long archiviati fuori record vengono copiati virtualmente.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Questo flag fa sì che il cursore si prepari per un inserimento dello stesso record e un'eliminazione o il record originale. Viene usato nei casi in cui la chiave primaria è stata modificata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
