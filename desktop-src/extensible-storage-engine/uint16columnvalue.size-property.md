---
description: 'Altre informazioni su: Proprietà UInt16ColumnValue. size'
title: Proprietà UInt16ColumnValue. size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt16ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint16columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104075
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60f61df594f564282e8c026d19bf64d83107de64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307797"
---
# <a name="uint16columnvaluesize-property"></a><span data-ttu-id="b5c1a-103">Proprietà UInt16ColumnValue. size</span><span class="sxs-lookup"><span data-stu-id="b5c1a-103">UInt16ColumnValue.Size property</span></span>

<span data-ttu-id="b5c1a-104">Ottiene la dimensione del valore nella colonna.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="b5c1a-105">Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="b5c1a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5c1a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5c1a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5c1a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c1a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c1a-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="b5c1a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b5c1a-109">Property value</span></span>

<span data-ttu-id="b5c1a-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b5c1a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b5c1a-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5c1a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5c1a-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b5c1a-112">Reference</span></span>

[<span data-ttu-id="b5c1a-113">Classe UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b5c1a-113">UInt16ColumnValue class</span></span>](./uint16columnvalue-class.md)

[<span data-ttu-id="b5c1a-114">Membri di UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b5c1a-114">UInt16ColumnValue members</span></span>](./uint16columnvalue-members.md)

[<span data-ttu-id="b5c1a-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b5c1a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
