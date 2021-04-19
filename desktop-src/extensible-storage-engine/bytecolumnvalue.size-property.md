---
description: 'Altre informazioni su: Proprietà ByteColumnValue. size'
title: Proprietà ByteColumnValue. size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94679812f0bdebd043bda3596fceffad6eb2fd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317521"
---
# <a name="bytecolumnvaluesize-property"></a><span data-ttu-id="f947d-103">Proprietà ByteColumnValue. size</span><span class="sxs-lookup"><span data-stu-id="f947d-103">ByteColumnValue.Size property</span></span>

<span data-ttu-id="f947d-104">Ottiene la dimensione del valore nella colonna.</span><span class="sxs-lookup"><span data-stu-id="f947d-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="f947d-105">Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="f947d-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="f947d-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f947d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f947d-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f947d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f947d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f947d-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="f947d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f947d-109">Property value</span></span>

<span data-ttu-id="f947d-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f947d-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f947d-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f947d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f947d-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f947d-112">Reference</span></span>

[<span data-ttu-id="f947d-113">Classe ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="f947d-113">ByteColumnValue class</span></span>](./bytecolumnvalue-class.md)

[<span data-ttu-id="f947d-114">Membri di ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="f947d-114">ByteColumnValue members</span></span>](./bytecolumnvalue-members.md)

[<span data-ttu-id="f947d-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f947d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
