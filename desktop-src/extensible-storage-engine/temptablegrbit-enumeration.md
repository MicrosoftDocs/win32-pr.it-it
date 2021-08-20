---
description: Altre informazioni sull'enumerazione TempTableGrbit
title: Enumerazione TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b97f8b736ff924254e7508b29b0841b48174b46526977f32a4f544181da09ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070846"
---
# <a name="temptablegrbit-enumeration"></a>Enumerazione TempTableGrbit

Opzioni per la creazione di tabelle temporanee.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>Indicizzato</td>
<td>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di JetSeek per la ricerca di record in base alla chiave di indice. Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</td>
</tr>
<tr class="odd">
<td></td>
<td>Univoco</td>
<td>Questa opzione richiede che i record con chiavi di indice duplicate siano rimossi dal set finale di record nella tabella temporanea. Prima di Windows Server 2003, il motore di database presupponeva sempre che questa opzione fosse attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A Windows Server 2003, è ora possibile creare una tabella temporanea che NON rimuove i duplicati quando viene specificata anche l'opzione <a href="dn351284(v=exchg.10).md">ForwardOnly.</a> Non è possibile sapere quale duplicato vincerà e quali duplicati verranno eliminati in generale. Tuttavia, quando viene richiesta l'opzione ErrorOnDuplicateInsertion, il primo record con una determinata chiave di indice da inserire nella tabella temporanea vincerà sempre.</td>
</tr>
<tr class="even">
<td></td>
<td>Aggiornabile</td>
<td>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire la successiva modifica dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</td>
</tr>
<tr class="odd">
<td></td>
<td>Scorrimento</td>
<td>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e direzione usando <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>. Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</td>
</tr>
<tr class="even">
<td></td>
<td>SortNullsHigh</td>
<td>Questa opzione richiede l'ordinamento dei valori di colonna chiave NULL più vicini alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceMaterialization</td>
<td>Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporta prestazioni migliorate.</td>
</tr>
<tr class="even">
<td></td>
<td>ErrorOnDuplicateInsertion</td>
<td>Questa opzione richiede che qualsiasi tentativo di inserimento di un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>. Se questa opzione non è richiesta, un duplicato può essere rilevato immediatamente e avere esito negativo o può essere rimosso automaticamente in un secondo momento a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta. Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[ForwardOnly](./server2003grbits.forwardonly-field.md)

[IntrinsicLVsOnly](./windows7grbits.intrinsiclvsonly-field.md)
