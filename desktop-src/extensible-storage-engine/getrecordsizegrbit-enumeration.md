---
description: 'Altre informazioni su: Enumerazione GetRecordSizeGrbit'
title: Enumerazione GetRecordSizeGrbit
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309168"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="e8aac-103">Enumerazione GetRecordSizeGrbit</span><span class="sxs-lookup"><span data-stu-id="e8aac-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="e8aac-104">Opzioni per [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="e8aac-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="e8aac-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="e8aac-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e8aac-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8aac-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8aac-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8aac-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8aac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8aac-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="e8aac-109">Members</span><span class="sxs-lookup"><span data-stu-id="e8aac-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e8aac-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="e8aac-110">Member name</span></span></th>
<th><span data-ttu-id="e8aac-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8aac-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e8aac-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="e8aac-112">None</span></span></td>
<td><span data-ttu-id="e8aac-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="e8aac-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e8aac-114">InCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="e8aac-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="e8aac-115">Recuperare le dimensioni del record che si trova nel buffer di copia preparato o aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e8aac-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="e8aac-116">In caso contrario, il TableID deve essere posizionato su un record e tale record verrà usato.</span><span class="sxs-lookup"><span data-stu-id="e8aac-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e8aac-117">RunningTotal</span><span class="sxs-lookup"><span data-stu-id="e8aac-117">RunningTotal</span></span></td>
<td><span data-ttu-id="e8aac-118">Il JET_RECSIZE non viene azzerato prima di riempire il contenuto, agendo effettivamente come un accumulo di statistiche per più record visitati o aggiornati.</span><span class="sxs-lookup"><span data-stu-id="e8aac-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e8aac-119">Locale</span><span class="sxs-lookup"><span data-stu-id="e8aac-119">Local</span></span></td>
<td><span data-ttu-id="e8aac-120">Ignorare i valori Long non intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e8aac-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="e8aac-121">Verrà utilizzato solo il record locale nella pagina.</span><span class="sxs-lookup"><span data-stu-id="e8aac-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e8aac-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8aac-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8aac-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e8aac-123">Reference</span></span>

[<span data-ttu-id="e8aac-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e8aac-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
