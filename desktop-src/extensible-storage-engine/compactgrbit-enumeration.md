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
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="1ed15-103">Enumerazione CompactGrbit</span><span class="sxs-lookup"><span data-stu-id="1ed15-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="1ed15-104">Opzioni per [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="1ed15-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="1ed15-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="1ed15-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1ed15-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ed15-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ed15-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ed15-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ed15-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="1ed15-109">Members</span><span class="sxs-lookup"><span data-stu-id="1ed15-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1ed15-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="1ed15-110">Member name</span></span></th>
<th><span data-ttu-id="1ed15-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ed15-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1ed15-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="1ed15-112">None</span></span></td>
<td><span data-ttu-id="1ed15-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="1ed15-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1ed15-114">Statistiche</span><span class="sxs-lookup"><span data-stu-id="1ed15-114">Stats</span></span></td>
<td><span data-ttu-id="1ed15-115">Consente a JetCompact di eseguire il dump delle statistiche nel database di origine in un file denominato DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="1ed15-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="1ed15-116">Le statistiche includono il nome di ogni tabella nel database di origine, il numero di righe in ogni tabella, le dimensioni totali in byte di tutte le righe di ogni tabella, le dimensioni totali in byte di tutte le colonne di tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a> che erano sufficientemente grandi da essere archiviate separate dal record, il numero di pagine foglia dell'indice cluster e il numero di pagine foglia di valore lungo.</span><span class="sxs-lookup"><span data-stu-id="1ed15-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="1ed15-117">Inoltre, le statistiche di riepilogo, incluse le dimensioni del database di origine, il database di destinazione, il tempo necessario per la compattazione del database, hanno anche tutti il dump dello spazio.</span><span class="sxs-lookup"><span data-stu-id="1ed15-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1ed15-118">Ripristina</span><span class="sxs-lookup"><span data-stu-id="1ed15-118">Repair</span></span></td>
<td><span data-ttu-id="1ed15-119"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="1ed15-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="1ed15-120">Utilizzato quando è noto che il database di origine è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1ed15-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="1ed15-121">Consente un intero set di nuovi comportamenti destinati a recuperare il maggior quantità possibile di dati dal database di origine.</span><span class="sxs-lookup"><span data-stu-id="1ed15-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="1ed15-122">JetCompact con questo set di opzioni può restituire <a href="hh564840(v=exchg.10).md">esito positivo</a> , ma non copiare tutti i dati creati nel database di origine.</span><span class="sxs-lookup"><span data-stu-id="1ed15-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="1ed15-123">I dati che si trovavano in parti danneggiate del database di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="1ed15-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1ed15-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ed15-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ed15-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1ed15-125">Reference</span></span>

[<span data-ttu-id="1ed15-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ed15-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
