---
description: 'Altre informazioni su: Enumerazione TermGrbit'
title: Enumerazione TermGrbit
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759086"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="7a737-103">Enumerazione TermGrbit</span><span class="sxs-lookup"><span data-stu-id="7a737-103">TermGrbit enumeration</span></span>

<span data-ttu-id="7a737-104">Opzioni per [JetTerm2 (JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a737-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="7a737-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="7a737-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7a737-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a737-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a737-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a737-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a737-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a737-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="7a737-109">Members</span><span class="sxs-lookup"><span data-stu-id="7a737-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7a737-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="7a737-110">Member name</span></span></th>
<th><span data-ttu-id="7a737-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a737-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7a737-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="7a737-112">None</span></span></td>
<td><span data-ttu-id="7a737-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="7a737-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7a737-114">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="7a737-114">Complete</span></span></td>
<td><span data-ttu-id="7a737-115">Richiede che l'istanza venga arrestata in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="7a737-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="7a737-116">Eventuali operazioni di pulizia facoltative normalmente eseguite in background in fase di esecuzione vengono completate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7a737-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7a737-117">Improvviso</span><span class="sxs-lookup"><span data-stu-id="7a737-117">Abrupt</span></span></td>
<td><span data-ttu-id="7a737-118">Richiede che l'istanza venga arrestata nel minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="7a737-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="7a737-119">Qualsiasi lavoro facoltativo che normalmente verrebbe eseguito in background in fase di esecuzione viene abbandonato.</span><span class="sxs-lookup"><span data-stu-id="7a737-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7a737-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a737-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a737-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7a737-121">Reference</span></span>

[<span data-ttu-id="7a737-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7a737-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="7a737-123">Sporco</span><span class="sxs-lookup"><span data-stu-id="7a737-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
