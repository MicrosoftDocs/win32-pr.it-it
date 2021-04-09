---
description: 'Altre informazioni su: Enumerazione JET_dbstate'
title: Enumerazione JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749882"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="02c34-103">Enumerazione JET_dbstate</span><span class="sxs-lookup"><span data-stu-id="02c34-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="02c34-104">Stati del database (utilizzati in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span><span class="sxs-lookup"><span data-stu-id="02c34-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="02c34-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02c34-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02c34-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02c34-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02c34-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02c34-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="02c34-108">Members</span><span class="sxs-lookup"><span data-stu-id="02c34-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="02c34-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="02c34-109">Member name</span></span></th>
<th><span data-ttu-id="02c34-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02c34-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="02c34-111">Blue Water Corporation</span><span class="sxs-lookup"><span data-stu-id="02c34-111">JustCreated</span></span></td>
<td><span data-ttu-id="02c34-112">Il database è stato appena creato.</span><span class="sxs-lookup"><span data-stu-id="02c34-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="02c34-113">DirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="02c34-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="02c34-114">Database di chiusura Dirty (non coerente).</span><span class="sxs-lookup"><span data-stu-id="02c34-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="02c34-115">CleanShutdown</span><span class="sxs-lookup"><span data-stu-id="02c34-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="02c34-116">Database di chiusura normale (coerente).</span><span class="sxs-lookup"><span data-stu-id="02c34-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="02c34-117">BeingConverted</span><span class="sxs-lookup"><span data-stu-id="02c34-117">BeingConverted</span></span></td>
<td><span data-ttu-id="02c34-118">È in corso la conversione del database.</span><span class="sxs-lookup"><span data-stu-id="02c34-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="02c34-119">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="02c34-119">ForceDetach</span></span></td>
<td><span data-ttu-id="02c34-120">Il database è stato scollegato forzatamente.</span><span class="sxs-lookup"><span data-stu-id="02c34-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="02c34-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c34-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02c34-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="02c34-122">Reference</span></span>

[<span data-ttu-id="02c34-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="02c34-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
