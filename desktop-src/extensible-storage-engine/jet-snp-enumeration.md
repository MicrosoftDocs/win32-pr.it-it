---
description: 'Altre informazioni su: Enumerazione JET_SNP'
title: Enumerazione JET_SNP
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305771"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="01c91-103">Enumerazione JET_SNP</span><span class="sxs-lookup"><span data-stu-id="01c91-103">JET_SNP enumeration</span></span>

<span data-ttu-id="01c91-104">Tipo di operazione per cui viene segnalato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="01c91-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="01c91-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01c91-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01c91-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01c91-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01c91-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01c91-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="01c91-108">Members</span><span class="sxs-lookup"><span data-stu-id="01c91-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="01c91-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="01c91-109">Member name</span></span></th>
<th><span data-ttu-id="01c91-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01c91-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="01c91-111">Ripristina</span><span class="sxs-lookup"><span data-stu-id="01c91-111">Repair</span></span></td>
<td><span data-ttu-id="01c91-112">Il callback è per un'opzione di correzione.</span><span class="sxs-lookup"><span data-stu-id="01c91-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="01c91-113">Compact</span><span class="sxs-lookup"><span data-stu-id="01c91-113">Compact</span></span></td>
<td><span data-ttu-id="01c91-114">Il callback è per la deframmentazione del database.</span><span class="sxs-lookup"><span data-stu-id="01c91-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="01c91-115">Restore</span><span class="sxs-lookup"><span data-stu-id="01c91-115">Restore</span></span></td>
<td><span data-ttu-id="01c91-116">Il callback è per le opzioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="01c91-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="01c91-117">Backup</span><span class="sxs-lookup"><span data-stu-id="01c91-117">Backup</span></span></td>
<td><span data-ttu-id="01c91-118">Il callback è per le opzioni di backup.</span><span class="sxs-lookup"><span data-stu-id="01c91-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="01c91-119">Scrub</span><span class="sxs-lookup"><span data-stu-id="01c91-119">Scrub</span></span></td>
<td><span data-ttu-id="01c91-120">Il callback è per lo zero del database.</span><span class="sxs-lookup"><span data-stu-id="01c91-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="01c91-121">UpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="01c91-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="01c91-122">Il callback è il processo di aggiornamento del formato di record di tutte le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="01c91-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="01c91-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c91-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01c91-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="01c91-124">Reference</span></span>

[<span data-ttu-id="01c91-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="01c91-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
