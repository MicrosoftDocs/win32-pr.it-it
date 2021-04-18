---
description: 'Altre informazioni su: Enumerazione GotoSecondaryIndexBookmarkGrbit'
title: Enumerazione GotoSecondaryIndexBookmarkGrbit
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309166"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="82cbe-103">Enumerazione GotoSecondaryIndexBookmarkGrbit</span><span class="sxs-lookup"><span data-stu-id="82cbe-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="82cbe-104">Opzioni per [JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="82cbe-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="82cbe-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="82cbe-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="82cbe-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82cbe-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82cbe-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82cbe-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82cbe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82cbe-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="82cbe-109">Members</span><span class="sxs-lookup"><span data-stu-id="82cbe-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="82cbe-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="82cbe-110">Member name</span></span></th>
<th><span data-ttu-id="82cbe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82cbe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82cbe-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="82cbe-112">None</span></span></td>
<td><span data-ttu-id="82cbe-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="82cbe-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82cbe-114">BookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="82cbe-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="82cbe-115">Nel caso in cui non sia più possibile trovare la voce di indice, il cursore viene lasciato posizionato in corrispondenza del punto in cui è stata trovata in precedenza la voce di indice.</span><span class="sxs-lookup"><span data-stu-id="82cbe-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="82cbe-116">L'operazione avrà comunque esito negativo con JET_errRecordDeleted; Tuttavia, sarà possibile passare alla voce di indice successiva o precedente relativa alla voce di indice mancante.</span><span class="sxs-lookup"><span data-stu-id="82cbe-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="82cbe-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82cbe-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82cbe-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="82cbe-118">Reference</span></span>

[<span data-ttu-id="82cbe-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82cbe-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
