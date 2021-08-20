---
description: Altre informazioni sull'enumerazione RetrieveColumnGrbit
title: Enumerazione RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bd59f610b2ff1423b82539c61eff3d9d770a03d6f8291a1bae53b372fff318f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890669"
---
# <a name="retrievecolumngrbit-enumeration"></a>Enumerazione RetrieveColumnGrbit

Opzioni per JetRetrieveColumn.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
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
<td>RetrieveCopy</td>
<td>Questo flag fa in modo che il recupero della colonna recuperi il valore modificato anziché il valore originale. Se il valore non è stato modificato, viene recuperato il valore originale. In questo modo, un valore non ancora inserito o aggiornato può essere recuperato durante l'operazione di inserimento o aggiornamento di un record.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveFromIndex</td>
<td>Questa opzione viene usata per recuperare i valori di colonna dall'indice, se possibile, senza accedere al record. In questo modo, è possibile evitare il caricamento non necessario dei record quando i dati necessari sono disponibili dalle voci di indice stesse.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveFromPrimaryBookmark</td>
<td>Questa opzione viene usata per recuperare i valori di colonna dal segnalibro dell'indice e può differire dal valore dell'indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario. Questo bit non può essere impostato se è impostato anche RetrieveFromIndex.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveTag</td>
<td>Questa opzione viene usata per recuperare il numero di sequenza di un valore di colonna multivalore in JET_RETINFO.itagSequence. Il recupero del numero di sequenza può essere un'operazione disserta e deve essere eseguita solo se necessario.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveNull</td>
<td>Questa opzione viene usata per recuperare valori NULL di colonna multivalore. Se questa opzione non viene specificata, i valori NULL di colonna multivalore verranno ignorati automaticamente.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveIgnoreDefault</td>
<td>Questa opzione influisce solo sulle colonne multivalore e determina la restituire un valore NULL quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
