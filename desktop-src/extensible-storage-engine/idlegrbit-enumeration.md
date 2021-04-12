---
description: 'Altre informazioni su: Enumerazione IdleGrbit'
title: Enumerazione IdleGrbit
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226550"
---
# <a name="idlegrbit-enumeration"></a><span data-ttu-id="53313-103">Enumerazione IdleGrbit</span><span class="sxs-lookup"><span data-stu-id="53313-103">IdleGrbit enumeration</span></span>

<span data-ttu-id="53313-104">Opzioni per [JetIdle (JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span><span class="sxs-lookup"><span data-stu-id="53313-104">Options for [JetIdle(JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span></span>

<span data-ttu-id="53313-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="53313-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="53313-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53313-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53313-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53313-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53313-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53313-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
```

## <a name="members"></a><span data-ttu-id="53313-109">Members</span><span class="sxs-lookup"><span data-stu-id="53313-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="53313-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="53313-110">Member name</span></span></th>
<th><span data-ttu-id="53313-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53313-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="53313-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="53313-112">None</span></span></td>
<td><span data-ttu-id="53313-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="53313-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="53313-114">FlushBuffers</span><span class="sxs-lookup"><span data-stu-id="53313-114">FlushBuffers</span></span></td>
<td><span data-ttu-id="53313-115">Attiva la pulizia dell'archivio delle versioni.</span><span class="sxs-lookup"><span data-stu-id="53313-115">Triggers cleanup of the version store.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="53313-116">Compact</span><span class="sxs-lookup"><span data-stu-id="53313-116">Compact</span></span></td>
<td><span data-ttu-id="53313-117">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="53313-117">Reserved for future use.</span></span> <span data-ttu-id="53313-118">Se questo flag è specificato, l'API restituirà <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="53313-118">If this flag is specified, the API will return <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="53313-119">GetStatus</span><span class="sxs-lookup"><span data-stu-id="53313-119">GetStatus</span></span></td>
<td><span data-ttu-id="53313-120">Restituisce <a href="hh557250(v=exchg.10).md">IdleFull</a> se l'archivio delle versioni è più della metà piena.</span><span class="sxs-lookup"><span data-stu-id="53313-120">Returns <a href="hh557250(v=exchg.10).md">IdleFull</a> if version store is more than half full.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="53313-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53313-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53313-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53313-122">Reference</span></span>

[<span data-ttu-id="53313-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53313-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
