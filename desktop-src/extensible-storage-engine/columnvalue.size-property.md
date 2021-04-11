---
description: 'Altre informazioni su: Proprietà ColumnValue. size'
title: Proprietà ColumnValue. size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101207
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20893eba6516b53045463ce664cdb77ae7e9b768
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049616"
---
# <a name="columnvaluesize-property"></a><span data-ttu-id="78978-103">Proprietà ColumnValue. size</span><span class="sxs-lookup"><span data-stu-id="78978-103">ColumnValue.Size property</span></span>

<span data-ttu-id="78978-104">Ottiene la dimensione del valore nella colonna.</span><span class="sxs-lookup"><span data-stu-id="78978-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="78978-105">Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="78978-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="78978-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78978-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="78978-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78978-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78978-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78978-108">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected abstract int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="78978-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78978-109">Property value</span></span>

<span data-ttu-id="78978-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="78978-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="78978-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78978-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78978-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="78978-112">Reference</span></span>

[<span data-ttu-id="78978-113">Classe ColumnValue</span><span class="sxs-lookup"><span data-stu-id="78978-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="78978-114">Membri di ColumnValue</span><span class="sxs-lookup"><span data-stu-id="78978-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="78978-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="78978-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
