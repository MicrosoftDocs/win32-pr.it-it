---
description: 'Altre informazioni su: Enumerazione CreateTableColumnIndexGrbit'
title: Enumerazione CreateTableColumnIndexGrbit
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968537"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="441dd-103">Enumerazione CreateTableColumnIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="441dd-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="441dd-104">Opzioni per JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="441dd-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="441dd-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="441dd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="441dd-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="441dd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="441dd-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="441dd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="441dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="441dd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="441dd-109">Members</span><span class="sxs-lookup"><span data-stu-id="441dd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="441dd-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="441dd-110">Member name</span></span></th>
<th><span data-ttu-id="441dd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="441dd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="441dd-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="441dd-112">None</span></span></td>
<td><span data-ttu-id="441dd-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="441dd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="441dd-114">FixedDDL</span><span class="sxs-lookup"><span data-stu-id="441dd-114">FixedDDL</span></span></td>
<td><span data-ttu-id="441dd-115">Il linguaggio DDL è fisso.</span><span class="sxs-lookup"><span data-stu-id="441dd-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="441dd-116">TemplateTable</span><span class="sxs-lookup"><span data-stu-id="441dd-116">TemplateTable</span></span></td>
<td><span data-ttu-id="441dd-117">Il linguaggio DDL è ereditabile.</span><span class="sxs-lookup"><span data-stu-id="441dd-117">The DDL is inheritable.</span></span> <span data-ttu-id="441dd-118">Implica FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="441dd-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="441dd-119">NoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="441dd-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="441dd-120">Utilizzato insieme a TemplateTable.</span><span class="sxs-lookup"><span data-stu-id="441dd-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="441dd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="441dd-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="441dd-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="441dd-122">Reference</span></span>

[<span data-ttu-id="441dd-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="441dd-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
