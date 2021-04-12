---
description: 'Altre informazioni su: Enumerazione EndExternalBackupGrbit'
title: Enumerazione EndExternalBackupGrbit
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233959"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="75c65-103">Enumerazione EndExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="75c65-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="75c65-104">Opzioni per [JetEndExternalBackupInstance (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="75c65-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="75c65-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="75c65-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="75c65-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75c65-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75c65-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75c65-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75c65-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75c65-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="75c65-109">Members</span><span class="sxs-lookup"><span data-stu-id="75c65-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="75c65-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="75c65-110">Member name</span></span></th>
<th><span data-ttu-id="75c65-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75c65-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75c65-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="75c65-112">None</span></span></td>
<td><span data-ttu-id="75c65-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="75c65-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75c65-114">Normale</span><span class="sxs-lookup"><span data-stu-id="75c65-114">Normal</span></span></td>
<td><span data-ttu-id="75c65-115">L'applicazione client ha completato completamente il backup e termina normalmente.</span><span class="sxs-lookup"><span data-stu-id="75c65-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75c65-116">Interruzione</span><span class="sxs-lookup"><span data-stu-id="75c65-116">Abort</span></span></td>
<td><span data-ttu-id="75c65-117">L'applicazione client sta interrompendo il backup.</span><span class="sxs-lookup"><span data-stu-id="75c65-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="75c65-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75c65-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75c65-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="75c65-119">Reference</span></span>

[<span data-ttu-id="75c65-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="75c65-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
