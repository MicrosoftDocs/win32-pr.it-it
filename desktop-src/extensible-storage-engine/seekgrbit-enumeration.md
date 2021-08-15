---
description: Altre informazioni sull'enumerazione SeekGrbit
title: Enumerazione SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12a65021d8c224d2a0ed50082b3120c94fc8c83f25c9aaf3eaf6e71d3f3f45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978591"
---
# <a name="seekgrbit-enumeration"></a>Enumerazione SeekGrbit

Opzioni per JetSeek.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che corrisponde esattamente alla chiave di ricerca.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice minore di una voce di indice che corrisponde esattamente ai criteri di ricerca.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice minore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore di una voce di indice che corrisponde esattamente ai criteri di ricerca.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Un intervallo di indici verrà automaticamente specificato per tutte le chiavi che corrispondono esattamente alla chiave di ricerca.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
