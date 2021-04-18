---
description: 'Altre informazioni su: Enumerazione PrereadIndexRangesGrbit'
title: Enumerazione PrereadIndexRangesGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313088"
---
# <a name="prereadindexrangesgrbit-enumeration"></a><span data-ttu-id="23373-103">Enumerazione PrereadIndexRangesGrbit</span><span class="sxs-lookup"><span data-stu-id="23373-103">PrereadIndexRangesGrbit enumeration</span></span>

<span data-ttu-id="23373-104">Opzioni per [JetPrereadIndexRanges (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, Int32, \[ \] , PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span><span class="sxs-lookup"><span data-stu-id="23373-104">Options for [JetPrereadIndexRanges(JET_SESID, JET_TABLEID, \[\], Int32, Int32, Int32, \[\], PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span></span>

<span data-ttu-id="23373-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="23373-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="23373-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23373-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="23373-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23373-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23373-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23373-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
```

## <a name="members"></a><span data-ttu-id="23373-109">Members</span><span class="sxs-lookup"><span data-stu-id="23373-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23373-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="23373-110">Member name</span></span></th>
<th><span data-ttu-id="23373-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23373-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23373-112">Inoltra</span><span class="sxs-lookup"><span data-stu-id="23373-112">Forward</span></span></td>
<td><span data-ttu-id="23373-113">Prelettura in futuro.</span><span class="sxs-lookup"><span data-stu-id="23373-113">Preread forward.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23373-114">Indietro</span><span class="sxs-lookup"><span data-stu-id="23373-114">Backwards</span></span></td>
<td><span data-ttu-id="23373-115">Prelettura all'indietro.</span><span class="sxs-lookup"><span data-stu-id="23373-115">Preread backwards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23373-116">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="23373-116">FirstPageOnly</span></span></td>
<td><span data-ttu-id="23373-117">Prelettura solo prima pagina di qualsiasi colonna di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="23373-117">Preread only first page of any long column.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23373-118">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="23373-118">NormalizedKey</span></span></td>
<td><span data-ttu-id="23373-119">Chiave/segnalibro normalizzato fornito al posto del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="23373-119">Normalized key/bookmark provided instead of column value.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="23373-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23373-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23373-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="23373-121">Reference</span></span>

[<span data-ttu-id="23373-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="23373-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
