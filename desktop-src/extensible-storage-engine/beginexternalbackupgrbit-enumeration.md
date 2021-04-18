---
description: 'Altre informazioni su: Enumerazione BeginExternalBackupGrbit'
title: Enumerazione BeginExternalBackupGrbit
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318461"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="8d552-103">Enumerazione BeginExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="8d552-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="8d552-104">Opzioni per [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="8d552-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="8d552-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="8d552-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8d552-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8d552-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8d552-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8d552-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8d552-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d552-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="8d552-109">Members</span><span class="sxs-lookup"><span data-stu-id="8d552-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8d552-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="8d552-110">Member name</span></span></th>
<th><span data-ttu-id="8d552-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d552-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8d552-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="8d552-112">None</span></span></td>
<td><span data-ttu-id="8d552-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="8d552-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8d552-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="8d552-114">Incremental</span></span></td>
<td><span data-ttu-id="8d552-115">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="8d552-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="8d552-116">Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="8d552-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8d552-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d552-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8d552-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8d552-118">Reference</span></span>

[<span data-ttu-id="8d552-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8d552-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
