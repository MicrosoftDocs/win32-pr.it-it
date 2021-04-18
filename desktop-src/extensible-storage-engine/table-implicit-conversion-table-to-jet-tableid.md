---
description: 'Altre informazioni su: conversione implicita di tabella (tabella per JET_TABLEID)'
title: Conversione implicita di tabella (da tabella a JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315067"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a><span data-ttu-id="f684f-103">Conversione implicita di tabella (da tabella a JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="f684f-103">Table Implicit conversion (Table to JET_TABLEID)</span></span>

<span data-ttu-id="f684f-104">Operatore di conversione implicito da una tabella a una JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="f684f-104">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="f684f-105">Ciò consente di usare una tabella con le API che prevedono un JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="f684f-105">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span>

<span data-ttu-id="f684f-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f684f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f684f-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f684f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f684f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f684f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a><span data-ttu-id="f684f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f684f-109">Parameters</span></span>

  - <span data-ttu-id="f684f-110">table</span><span class="sxs-lookup"><span data-stu-id="f684f-110">table</span></span>  
    <span data-ttu-id="f684f-111">Tipo: [Microsoft. ISAM. esent. Interop. Table](./table-class.md)</span><span class="sxs-lookup"><span data-stu-id="f684f-111">Type: [Microsoft.Isam.Esent.Interop.Table](./table-class.md)</span></span>  
    
    <span data-ttu-id="f684f-112">Tabella da convertire.</span><span class="sxs-lookup"><span data-stu-id="f684f-112">The table to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f684f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f684f-113">Return value</span></span>

<span data-ttu-id="f684f-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f684f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
<span data-ttu-id="f684f-115">JET_TABLEID della tabella.</span><span class="sxs-lookup"><span data-stu-id="f684f-115">The JET_TABLEID of the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f684f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f684f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f684f-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f684f-117">Reference</span></span>

[<span data-ttu-id="f684f-118">Classe Table</span><span class="sxs-lookup"><span data-stu-id="f684f-118">Table class</span></span>](./table-class.md)

[<span data-ttu-id="f684f-119">Membri della tabella</span><span class="sxs-lookup"><span data-stu-id="f684f-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="f684f-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f684f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
