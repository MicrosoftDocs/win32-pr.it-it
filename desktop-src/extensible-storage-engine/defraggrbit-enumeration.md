---
description: 'Altre informazioni su: Enumerazione DefragGrbit'
title: Enumerazione DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319790"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="d9385-103">Enumerazione DefragGrbit</span><span class="sxs-lookup"><span data-stu-id="d9385-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="d9385-104">Opzioni per [JetDefragment (JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="d9385-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="d9385-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="d9385-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d9385-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9385-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9385-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9385-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9385-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9385-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="d9385-109">Members</span><span class="sxs-lookup"><span data-stu-id="d9385-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d9385-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d9385-110">Member name</span></span></th>
<th><span data-ttu-id="d9385-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9385-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9385-112">AvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="d9385-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="d9385-113">Deframmenta la porzione di spazio disponibile nell'allocazione dello spazio del database ESE.</span><span class="sxs-lookup"><span data-stu-id="d9385-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="d9385-114">Lo spazio del database è suddiviso in due tipi, spazio di proprietà e spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="d9385-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="d9385-115">Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'utilizzo rispettivamente nella tabella o nell'indice.</span><span class="sxs-lookup"><span data-stu-id="d9385-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="d9385-116">Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea più che lo spazio di proprietà o i dati di tabella o di indice.</span><span class="sxs-lookup"><span data-stu-id="d9385-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9385-117">BatchStart</span><span class="sxs-lookup"><span data-stu-id="d9385-117">BatchStart</span></span></td>
<td><span data-ttu-id="d9385-118">Avvia una nuova attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="d9385-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9385-119">BatchStop</span><span class="sxs-lookup"><span data-stu-id="d9385-119">BatchStop</span></span></td>
<td><span data-ttu-id="d9385-120">Arresta un'attività di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="d9385-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d9385-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9385-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9385-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d9385-122">Reference</span></span>

[<span data-ttu-id="d9385-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9385-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
