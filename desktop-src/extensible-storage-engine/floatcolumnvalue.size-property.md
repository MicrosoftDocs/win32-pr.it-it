---
description: 'Altre informazioni su: Proprietà FloatColumnValue. size'
title: Proprietà FloatColumnValue. size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103243
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 259701daaad1027d06bf4c28c52084dae0b062b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309169"
---
# <a name="floatcolumnvaluesize-property"></a><span data-ttu-id="a8e3e-103">Proprietà FloatColumnValue. size</span><span class="sxs-lookup"><span data-stu-id="a8e3e-103">FloatColumnValue.Size property</span></span>

<span data-ttu-id="a8e3e-104">Ottiene la dimensione del valore nella colonna.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="a8e3e-105">Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="a8e3e-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="a8e3e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a8e3e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a8e3e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a8e3e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e3e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8e3e-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="a8e3e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a8e3e-109">Property value</span></span>

<span data-ttu-id="a8e3e-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a8e3e-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a8e3e-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8e3e-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a8e3e-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a8e3e-112">Reference</span></span>

[<span data-ttu-id="a8e3e-113">Classe FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="a8e3e-113">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="a8e3e-114">Membri di FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="a8e3e-114">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="a8e3e-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a8e3e-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
