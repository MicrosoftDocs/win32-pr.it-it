---
description: 'Altre informazioni su: JET_ENUMCOLUMNVALUE Class'
title: Classe JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305783"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="663fb-103">Classe JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="663fb-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="663fb-104">Enumera i valori di colonna di un record utilizzando la funzione JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="663fb-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="663fb-105">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) restituisce una matrice di strutture JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="663fb-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="663fb-106">La matrice viene restituita nella memoria allocata utilizzando il callback fornito a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="663fb-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="663fb-107">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="663fb-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="663fb-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="663fb-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="663fb-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="663fb-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="663fb-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="663fb-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="663fb-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="663fb-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="663fb-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="663fb-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="663fb-113">Thread safety</span><span class="sxs-lookup"><span data-stu-id="663fb-113">Thread safety</span></span>

<span data-ttu-id="663fb-114">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="663fb-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="663fb-115">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="663fb-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="663fb-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="663fb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="663fb-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="663fb-117">Reference</span></span>

[<span data-ttu-id="663fb-118">Membri JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="663fb-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="663fb-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="663fb-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
