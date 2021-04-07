---
description: 'Altre informazioni su: Enumerazione ObjectInfoFlags'
title: Enumerazione ObjectInfoFlags
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882266"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="54858-103">Enumerazione ObjectInfoFlags</span><span class="sxs-lookup"><span data-stu-id="54858-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="54858-104">Flag per oggetti ESENT (tabelle).</span><span class="sxs-lookup"><span data-stu-id="54858-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="54858-105">Utilizzato in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="54858-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="54858-106">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="54858-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="54858-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54858-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54858-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54858-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54858-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54858-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="54858-110">Members</span><span class="sxs-lookup"><span data-stu-id="54858-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="54858-111">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="54858-111">Member name</span></span></th>
<th><span data-ttu-id="54858-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54858-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="54858-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="54858-113">None</span></span></td>
<td><span data-ttu-id="54858-114">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="54858-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="54858-115">Sistema</span><span class="sxs-lookup"><span data-stu-id="54858-115">System</span></span></td>
<td><span data-ttu-id="54858-116">L'oggetto è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="54858-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="54858-117">TableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="54858-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="54858-118">La DDL della tabella è fissa.</span><span class="sxs-lookup"><span data-stu-id="54858-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="54858-119">TableTemplate</span><span class="sxs-lookup"><span data-stu-id="54858-119">TableTemplate</span></span></td>
<td><span data-ttu-id="54858-120">La DDL della tabella è ereditabile.</span><span class="sxs-lookup"><span data-stu-id="54858-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="54858-121">TableDerived</span><span class="sxs-lookup"><span data-stu-id="54858-121">TableDerived</span></span></td>
<td><span data-ttu-id="54858-122">La DDL della tabella viene ereditata da una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="54858-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="54858-123">TableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="54858-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="54858-124">Colonne fisse o variabili nelle tabelle derivate. in questo modo è possibile aggiungere colonne fisse o variabili al modello in futuro.</span><span class="sxs-lookup"><span data-stu-id="54858-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="54858-125">Utilizzato insieme a TableTemplate.</span><span class="sxs-lookup"><span data-stu-id="54858-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="54858-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54858-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54858-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="54858-127">Reference</span></span>

[<span data-ttu-id="54858-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="54858-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
