---
description: 'Altre informazioni su: Enumerazione DetachDatabaseGrbit'
title: Enumerazione DetachDatabaseGrbit
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233774"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="eed6b-103">Enumerazione DetachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="eed6b-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="eed6b-104">Opzioni per [JetDetachDatabase2 (JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span><span class="sxs-lookup"><span data-stu-id="eed6b-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="eed6b-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="eed6b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="eed6b-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eed6b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eed6b-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eed6b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eed6b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eed6b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="eed6b-109">Members</span><span class="sxs-lookup"><span data-stu-id="eed6b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="eed6b-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="eed6b-110">Member name</span></span></th>
<th><span data-ttu-id="eed6b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eed6b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="eed6b-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="eed6b-112">None</span></span></td>
<td><span data-ttu-id="eed6b-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="eed6b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="eed6b-114">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="eed6b-114">ForceDetach</span></span></td>
<td><span data-ttu-id="eed6b-115"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="eed6b-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="eed6b-116">Se si usa ForceDetach, viene restituito <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> .</span><span class="sxs-lookup"><span data-stu-id="eed6b-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="eed6b-117">Chiusura forzata</span><span class="sxs-lookup"><span data-stu-id="eed6b-117">ForceClose</span></span></td>
<td><span data-ttu-id="eed6b-118"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="eed6b-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="eed6b-119">Chiusura forzata non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="eed6b-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="eed6b-120">ForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="eed6b-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="eed6b-121"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="eed6b-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="eed6b-122">Se si usa ForceCloseAndDetach, viene restituito <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> .</span><span class="sxs-lookup"><span data-stu-id="eed6b-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="eed6b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eed6b-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eed6b-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="eed6b-124">Reference</span></span>

[<span data-ttu-id="eed6b-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eed6b-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
