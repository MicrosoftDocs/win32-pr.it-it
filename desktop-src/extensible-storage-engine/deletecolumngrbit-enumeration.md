---
description: 'Altre informazioni su: Enumerazione DeleteColumnGrbit'
title: Enumerazione DeleteColumnGrbit
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308550"
---
# <a name="deletecolumngrbit-enumeration"></a><span data-ttu-id="d8e28-103">Enumerazione DeleteColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="d8e28-103">DeleteColumnGrbit enumeration</span></span>

<span data-ttu-id="d8e28-104">Opzioni per [JetDeleteColumn2 (JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span><span class="sxs-lookup"><span data-stu-id="d8e28-104">Options for [JetDeleteColumn2(JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span></span>

<span data-ttu-id="d8e28-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="d8e28-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d8e28-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d8e28-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d8e28-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d8e28-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e28-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8e28-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
```

## <a name="members"></a><span data-ttu-id="d8e28-109">Members</span><span class="sxs-lookup"><span data-stu-id="d8e28-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d8e28-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d8e28-110">Member name</span></span></th>
<th><span data-ttu-id="d8e28-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8e28-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d8e28-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="d8e28-112">None</span></span></td>
<td><span data-ttu-id="d8e28-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="d8e28-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d8e28-114">IgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="d8e28-114">IgnoreTemplateColumns</span></span></td>
<td><span data-ttu-id="d8e28-115">L'API deve solo tentare di eliminare le colonne nella tabella derivata.</span><span class="sxs-lookup"><span data-stu-id="d8e28-115">The API should only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="d8e28-116">Se una colonna con tale nome esiste nella tabella di base, verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="d8e28-116">If a column of that name exists in the base table it will be ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d8e28-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e28-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d8e28-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d8e28-118">Reference</span></span>

[<span data-ttu-id="d8e28-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d8e28-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
