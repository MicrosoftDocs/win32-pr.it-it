---
description: 'Altre informazioni su: Enumerazione CompactGrbit'
title: Enumerazione CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308558"
---
# <a name="compactgrbit-enumeration"></a>Enumerazione CompactGrbit

Opzioni per [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Statistiche</td>
<td>Consente a JetCompact di eseguire il dump delle statistiche nel database di origine in un file denominato DFRGINFO.TXT. Le statistiche includono il nome di ogni tabella nel database di origine, il numero di righe in ogni tabella, le dimensioni totali in byte di tutte le righe di ogni tabella, le dimensioni totali in byte di tutte le colonne di tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a> che erano sufficientemente grandi da essere archiviate separate dal record, il numero di pagine foglia dell'indice cluster e il numero di pagine foglia di valore lungo. Inoltre, le statistiche di riepilogo, incluse le dimensioni del database di origine, il database di destinazione, il tempo necessario per la compattazione del database, hanno anche tutti il dump dello spazio.</td>
</tr>
<tr class="odd">
<td></td>
<td>Ripristina</td>
<td><strong>Obsoleto.</strong> Utilizzato quando è noto che il database di origine è danneggiato. Consente un intero set di nuovi comportamenti destinati a recuperare il maggior quantità possibile di dati dal database di origine. JetCompact con questo set di opzioni può restituire <a href="hh564840(v=exchg.10).md">esito positivo</a> , ma non copiare tutti i dati creati nel database di origine. I dati che si trovavano in parti danneggiate del database di origine verranno ignorati.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
