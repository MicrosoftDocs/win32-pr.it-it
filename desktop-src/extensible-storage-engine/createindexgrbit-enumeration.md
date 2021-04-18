---
description: 'Altre informazioni su: Enumerazione CreateIndexGrbit'
title: Enumerazione CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318812"
---
# <a name="createindexgrbit-enumeration"></a>Enumerazione CreateIndexGrbit

Opzioni per JetCreateIndex.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>nessuno</td>
<td>Opzioni predefinite.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnique</td>
<td>Le voci di indice (chiavi) duplicate non sono consentite. Questa operazione viene applicata quando viene chiamato JetUpdate, non quando viene chiamato JetSetColumn.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexPrimary</td>
<td>L'indice è un indice primario (cluster). Ogni tabella deve avere esattamente un indice primario. Se nessun indice primario viene definito in modo esplicito su una tabella, il motore di database creerà il proprio indice primario.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexDisallowNull</td>
<td>Nessuna delle colonne in cui viene creato l'indice può contenere un valore NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreNull</td>
<td>Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexIgnoreAnyNull</td>
<td>Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreFirstNull</td>
<td>Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexLazyFlush</td>
<td>Specifica che le operazioni sugli indici verranno registrate in modalità differita. JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati. Se le operazioni di indicizzazione vengono interrotte dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere il database in uno stato coerente, ma l'indice potrebbe non essere presente.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexEmpty</td>
<td>Non tentare di compilare l'indice perché tutte le voci restituiscono NULL. grbit deve inoltre specificare JET_bitIgnoreAnyNull quando viene passato JET_bitIndexEmpty. Si tratta di un miglioramento delle prestazioni. Se, ad esempio, viene aggiunta una nuova colonna a una tabella, viene creato un indice sulla colonna appena aggiunta, tutti i record della tabella verranno analizzati anche se non vengono mai aggiunti all'indice. La specifica di JET_bitIndexEmpty ignora l'analisi della tabella, che potrebbe richiedere molto tempo.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnversioned</td>
<td>Causa la visibilità della creazione dell'indice in altre transazioni. In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione. Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice, in modo che la seconda creazione dell'indice avrà esito negativo anziché causare potenzialmente molte operazioni di database non necessarie. La seconda transazione potrebbe non essere in grado di utilizzare immediatamente l'indice. È necessario completare l'operazione di creazione dell'indice prima che sia utilizzabile. La sessione non deve attualmente trovarsi in una transazione per creare un indice senza informazioni sulla versione.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexSortNullsHigh</td>
<td>Se si specifica questo flag, i valori NULL verranno ordinati dopo i dati per tutte le colonne dell'indice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
