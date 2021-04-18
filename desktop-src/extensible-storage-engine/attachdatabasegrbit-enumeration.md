---
description: 'Altre informazioni su: Enumerazione AttachDatabaseGrbit'
title: Enumerazione AttachDatabaseGrbit
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319280"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="deeda-103">Enumerazione AttachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="deeda-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="deeda-104">Opzioni per JetAttachDatabase.</span><span class="sxs-lookup"><span data-stu-id="deeda-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="deeda-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="deeda-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="deeda-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="deeda-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="deeda-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="deeda-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="deeda-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deeda-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="deeda-109">Members</span><span class="sxs-lookup"><span data-stu-id="deeda-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="deeda-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="deeda-110">Member name</span></span></th>
<th><span data-ttu-id="deeda-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="deeda-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="deeda-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="deeda-112">None</span></span></td>
<td><span data-ttu-id="deeda-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="deeda-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="deeda-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="deeda-114">ReadOnly</span></span></td>
<td><span data-ttu-id="deeda-115">Impedisce le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="deeda-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="deeda-116">DeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="deeda-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="deeda-117">Se JET_paramEnableIndexChecking è stato impostato, verranno eliminati tutti gli indici sui dati Unicode.</span><span class="sxs-lookup"><span data-stu-id="deeda-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="deeda-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deeda-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="deeda-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="deeda-119">Reference</span></span>

[<span data-ttu-id="deeda-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="deeda-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
