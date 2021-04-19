---
description: 'Altre informazioni su: Proprietà ColumnValue. length'
title: Proprietà ColumnValue. length
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319795"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="a4748-103">Proprietà ColumnValue. length</span><span class="sxs-lookup"><span data-stu-id="a4748-103">ColumnValue.Length property</span></span>

<span data-ttu-id="a4748-104">Ottiene la lunghezza in byte di un valore di colonna, che è zero se la colonna è null; in caso contrario, corrisponde alla dimensione per le colonne a dimensione fissa e rappresenta la lunghezza in byte effettivo del valore per le colonne di dimensioni variabili, ad esempio binario e stringa.</span><span class="sxs-lookup"><span data-stu-id="a4748-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="a4748-105">Per le stringhe la lunghezza viene determinata in base al presupposto di due byte per carattere.</span><span class="sxs-lookup"><span data-stu-id="a4748-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="a4748-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4748-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4748-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4748-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4748-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4748-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="a4748-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a4748-109">Property value</span></span>

<span data-ttu-id="a4748-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a4748-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a4748-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4748-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4748-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a4748-112">Reference</span></span>

[<span data-ttu-id="a4748-113">Classe ColumnValue</span><span class="sxs-lookup"><span data-stu-id="a4748-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="a4748-114">Membri di ColumnValue</span><span class="sxs-lookup"><span data-stu-id="a4748-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="a4748-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a4748-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
