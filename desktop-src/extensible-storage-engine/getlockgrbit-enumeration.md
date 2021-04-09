---
description: 'Altre informazioni su: Enumerazione GetLockGrbit'
title: Enumerazione GetLockGrbit
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966999"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="7f9a3-103">Enumerazione GetLockGrbit</span><span class="sxs-lookup"><span data-stu-id="7f9a3-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="7f9a3-104">Opzioni per JetGetLock.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-104">Options for JetGetLock.</span></span>

<span data-ttu-id="7f9a3-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7f9a3-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f9a3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f9a3-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f9a3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9a3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f9a3-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="7f9a3-109">Members</span><span class="sxs-lookup"><span data-stu-id="7f9a3-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7f9a3-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="7f9a3-110">Member name</span></span></th>
<th><span data-ttu-id="7f9a3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f9a3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7f9a3-112">Lettura</span><span class="sxs-lookup"><span data-stu-id="7f9a3-112">Read</span></span></td>
<td><span data-ttu-id="7f9a3-113">Acquisisce un blocco di lettura sul record corrente.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="7f9a3-114">I blocchi di lettura non sono compatibili con i blocchi di scrittura già conservati da altre sessioni, ma sono compatibili con i blocchi di lettura mantenuti da altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7f9a3-115">Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f9a3-115">Write</span></span></td>
<td><span data-ttu-id="7f9a3-116">Acquisisce un blocco di scrittura nel record corrente.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="7f9a3-117">I blocchi di scrittura non sono compatibili con i blocchi Write o Read utilizzati da altre sessioni, ma sono compatibili con i blocchi di lettura contenuti nella stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7f9a3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f9a3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f9a3-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7f9a3-119">Reference</span></span>

[<span data-ttu-id="7f9a3-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7f9a3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
