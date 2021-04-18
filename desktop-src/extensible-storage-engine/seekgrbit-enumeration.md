---
description: 'Altre informazioni su: Enumerazione SeekGrbit'
title: Enumerazione SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313074"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="2db30-103">Enumerazione SeekGrbit</span><span class="sxs-lookup"><span data-stu-id="2db30-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="2db30-104">Opzioni per JetSeek.</span><span class="sxs-lookup"><span data-stu-id="2db30-104">Options for JetSeek.</span></span>

<span data-ttu-id="2db30-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="2db30-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="2db30-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2db30-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2db30-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2db30-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2db30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2db30-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="2db30-109">Members</span><span class="sxs-lookup"><span data-stu-id="2db30-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2db30-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="2db30-110">Member name</span></span></th>
<th><span data-ttu-id="2db30-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2db30-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2db30-112">SeekEQ</span><span class="sxs-lookup"><span data-stu-id="2db30-112">SeekEQ</span></span></td>
<td><span data-ttu-id="2db30-113">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che corrisponde esattamente alla chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2db30-114">SeekLT</span><span class="sxs-lookup"><span data-stu-id="2db30-114">SeekLT</span></span></td>
<td><span data-ttu-id="2db30-115">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice inferiore a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2db30-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="2db30-116">SeekLE</span></span></td>
<td><span data-ttu-id="2db30-117">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice che è minore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2db30-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="2db30-118">SeekGE</span></span></td>
<td><span data-ttu-id="2db30-119">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che è maggiore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2db30-120">SeekGT</span><span class="sxs-lookup"><span data-stu-id="2db30-120">SeekGT</span></span></td>
<td><span data-ttu-id="2db30-121">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore di una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2db30-122">SetIndexRange</span><span class="sxs-lookup"><span data-stu-id="2db30-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="2db30-123">Un intervallo di indici verrà automaticamente configurato per tutte le chiavi che corrispondono esattamente alla chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db30-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2db30-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2db30-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2db30-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2db30-125">Reference</span></span>

[<span data-ttu-id="2db30-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2db30-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
