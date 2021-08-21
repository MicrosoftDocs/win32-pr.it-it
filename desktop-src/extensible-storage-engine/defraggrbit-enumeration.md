---
description: Altre informazioni sull'enumerazione DefragGrbit
title: Enumerazione DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faf2187a47f7a3cd519d69c8cf45f377a4e0f0941d4e9a83bd50653cc4236504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083438"
---
# <a name="defraggrbit-enumeration"></a>Enumerazione DefragGrbit

Opzioni per [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
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
<td>AvailSpaceTreesOnly</td>
<td>Deframmenta la parte di spazio disponibile dell'allocazione dello spazio del database ESE. Lo spazio del database è suddiviso in due tipi: spazio di proprietà e spazio disponibile. Lo spazio di proprietà viene allocato a una tabella o a un indice mentre lo spazio disponibile è pronto per l'uso rispettivamente all'interno della tabella o dell'indice. Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea più dello spazio di proprietà o dei dati della tabella o dell'indice.</td>
</tr>
<tr class="even">
<td></td>
<td>Avvio di Batch</td>
<td>Avvia una nuova attività di deframmentazione.</td>
</tr>
<tr class="odd">
<td></td>
<td>BatchStop</td>
<td>Arresta un'attività di deframmentazione.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
