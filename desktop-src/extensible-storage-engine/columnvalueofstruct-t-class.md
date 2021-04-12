---
description: 'Altre informazioni su: <T> classe ColumnValueOfStruct'
title: Classe ColumnValueOfStruct (T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351091"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="8abac-103">\<T\>Classe ColumnValueOfStruct</span><span class="sxs-lookup"><span data-stu-id="8abac-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="8abac-104">Impostare una colonna di tipo struct (ad esempio, Int32/GUID).</span><span class="sxs-lookup"><span data-stu-id="8abac-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8abac-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="8abac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8abac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8abac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8abac-107">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="8abac-108">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="8abac-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="8abac-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8abac-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8abac-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8abac-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8abac-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8abac-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="8abac-112">Parametri di tipo</span><span class="sxs-lookup"><span data-stu-id="8abac-112">Type parameters</span></span>

  - <span data-ttu-id="8abac-113">T</span><span class="sxs-lookup"><span data-stu-id="8abac-113">T</span></span>  
    <span data-ttu-id="8abac-114">Tipo da impostare.</span><span class="sxs-lookup"><span data-stu-id="8abac-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="8abac-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="8abac-115">Thread safety</span></span>

<span data-ttu-id="8abac-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8abac-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8abac-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8abac-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8abac-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8abac-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8abac-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8abac-119">Reference</span></span>

[<span data-ttu-id="8abac-120">Membri di ColumnValueOfStruct \<T\></span><span class="sxs-lookup"><span data-stu-id="8abac-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="8abac-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8abac-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="8abac-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="8abac-122">Derived types</span></span>

[<span data-ttu-id="8abac-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="8abac-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8abac-124">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="8abac-125">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="8abac-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="8abac-126">Microsoft. ISAM. esent. Interop. BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="8abac-127">Microsoft. ISAM. esent. Interop. ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="8abac-128">Microsoft. ISAM. esent. Interop. DateTimeColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="8abac-129">Microsoft. ISAM. esent. Interop. DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="8abac-130">Microsoft. ISAM. esent. Interop. FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="8abac-131">Microsoft. ISAM. esent. Interop. GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="8abac-132">Microsoft. ISAM. esent. Interop. Int16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="8abac-133">Microsoft. ISAM. esent. Interop. Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="8abac-134">Microsoft. ISAM. esent. Interop. Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="8abac-135">Microsoft. ISAM. esent. Interop. UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="8abac-136">Microsoft. ISAM. esent. Interop. UInt32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="8abac-137">Microsoft. ISAM. esent. Interop. UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="8abac-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)