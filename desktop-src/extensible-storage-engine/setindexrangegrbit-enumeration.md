---
description: 'Altre informazioni su: Enumerazione SetIndexRangeGrbit'
title: Enumerazione SetIndexRangeGrbit
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308014"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="8e2a3-103">Enumerazione SetIndexRangeGrbit</span><span class="sxs-lookup"><span data-stu-id="8e2a3-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="8e2a3-104">Opzioni per JetSetIndexRange.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="8e2a3-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8e2a3-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e2a3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e2a3-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e2a3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2a3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2a3-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="8e2a3-109">Members</span><span class="sxs-lookup"><span data-stu-id="8e2a3-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8e2a3-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="8e2a3-110">Member name</span></span></th>
<th><span data-ttu-id="8e2a3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e2a3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e2a3-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="8e2a3-112">None</span></span></td>
<td><span data-ttu-id="8e2a3-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e2a3-114">RangeInclusive</span><span class="sxs-lookup"><span data-stu-id="8e2a3-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="8e2a3-115">Questa opzione indica che il limite dell'intervallo di indici è incluso.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e2a3-116">RangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="8e2a3-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="8e2a3-117">La chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina alla fine dell'indice che corrisponderà all'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e2a3-118">RangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="8e2a3-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="8e2a3-119">L'intervallo di indici deve essere rimosso non appena è stato stabilito.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="8e2a3-120">Questa operazione è utile per verificare l'esistenza di voci di indice che corrispondono ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e2a3-121">RangeRemove</span><span class="sxs-lookup"><span data-stu-id="8e2a3-121">RangeRemove</span></span></td>
<td><span data-ttu-id="8e2a3-122">Annulla e intervallo di indici esistente.</span><span class="sxs-lookup"><span data-stu-id="8e2a3-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8e2a3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e2a3-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e2a3-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8e2a3-124">Reference</span></span>

[<span data-ttu-id="8e2a3-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8e2a3-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
