---
description: Altre informazioni sull'enumerazione CrashDumpGrbit
title: Enumerazione CrashDumpGrbit (Microsoft.Isam.Esent.Interop.Windows7)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cad58cac50d42b7abaadb179b4068bda2534383113b48430c79d874357c030c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083485"
---
# <a name="crashdumpgrbit-enumeration"></a>Enumerazione CrashDumpGrbit

Opzioni per JetConfigureProcessForCrashDump.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
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
<td>Minimo</td>
<td>Il dump minimo include CacheMinimum.</td>
</tr>
<tr class="odd">
<td></td>
<td>Massimo</td>
<td>Il valore massimo di dump include CacheMaximum.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheMinimum</td>
<td>CacheMinimum include pagine con latch. CacheMinimum include le pagine usate per la memoria. CacheMinimum include pagine contrassegnate con errori.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheMaximum</td>
<td>Il valore massimo della cache include il valore minimo della cache. Il valore massimo della cache include l'intera immagine della cache.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeDirtyPages</td>
<td>Il dump include le pagine modificate.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheIncludeCachedPages</td>
<td>Il dump include pagine che contengono dati validi.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeCorruptedPages</td>
<td>Il dump include pagine danneggiate (costo di calcolo elevato).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
