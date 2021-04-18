---
description: 'Altre informazioni su: Enumerazione BackupGrbit'
title: Enumerazione BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318464"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="c6d25-103">Enumerazione BackupGrbit</span><span class="sxs-lookup"><span data-stu-id="c6d25-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="c6d25-104">Opzioni per [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="c6d25-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="c6d25-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="c6d25-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c6d25-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c6d25-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c6d25-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c6d25-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d25-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6d25-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="c6d25-109">Members</span><span class="sxs-lookup"><span data-stu-id="c6d25-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c6d25-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="c6d25-110">Member name</span></span></th>
<th><span data-ttu-id="c6d25-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6d25-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c6d25-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="c6d25-112">None</span></span></td>
<td><span data-ttu-id="c6d25-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="c6d25-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c6d25-114">Incremental</span><span class="sxs-lookup"><span data-stu-id="c6d25-114">Incremental</span></span></td>
<td><span data-ttu-id="c6d25-115">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="c6d25-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="c6d25-116">Ciò significa che verrà eseguito il backup solo dei file di log creati dopo l'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="c6d25-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c6d25-117">Atomica</span><span class="sxs-lookup"><span data-stu-id="c6d25-117">Atomic</span></span></td>
<td><span data-ttu-id="c6d25-118">Crea un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="c6d25-118">Creates a full backup of the database.</span></span> <span data-ttu-id="c6d25-119">In questo modo è possibile mantenere un backup esistente nella stessa directory se il nuovo backup non riesce.</span><span class="sxs-lookup"><span data-stu-id="c6d25-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c6d25-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6d25-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c6d25-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c6d25-121">Reference</span></span>

[<span data-ttu-id="c6d25-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c6d25-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
