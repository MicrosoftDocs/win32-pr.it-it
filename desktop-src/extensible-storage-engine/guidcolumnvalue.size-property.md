---
description: 'Altre informazioni su: Proprietà GuidColumnValue. size'
title: Proprietà GuidColumnValue. size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55107387
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b973638ac8caa4848ed5ecc65468c363ebd2f866
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309160"
---
# <a name="guidcolumnvaluesize-property"></a><span data-ttu-id="fe124-103">Proprietà GuidColumnValue. size</span><span class="sxs-lookup"><span data-stu-id="fe124-103">GuidColumnValue.Size property</span></span>

<span data-ttu-id="fe124-104">Ottiene la dimensione del valore nella colonna.</span><span class="sxs-lookup"><span data-stu-id="fe124-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="fe124-105">Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="fe124-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="fe124-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fe124-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fe124-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fe124-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fe124-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe124-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="fe124-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fe124-109">Property value</span></span>

<span data-ttu-id="fe124-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fe124-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe124-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe124-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fe124-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="fe124-112">Reference</span></span>

[<span data-ttu-id="fe124-113">Classe GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="fe124-113">GuidColumnValue class</span></span>](./guidcolumnvalue-class.md)

[<span data-ttu-id="fe124-114">Membri di GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="fe124-114">GuidColumnValue members</span></span>](./guidcolumnvalue-members.md)

[<span data-ttu-id="fe124-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fe124-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
