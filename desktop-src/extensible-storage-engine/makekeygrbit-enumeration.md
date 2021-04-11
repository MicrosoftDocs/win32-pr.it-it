---
description: 'Altre informazioni su: Enumerazione MakeKeyGrbit'
title: Enumerazione MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128626"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="a39a8-103">Enumerazione MakeKeyGrbit</span><span class="sxs-lookup"><span data-stu-id="a39a8-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="a39a8-104">Opzioni per JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="a39a8-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="a39a8-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="a39a8-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a39a8-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a39a8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a39a8-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a39a8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a39a8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a39a8-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="a39a8-109">Members</span><span class="sxs-lookup"><span data-stu-id="a39a8-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a39a8-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="a39a8-110">Member name</span></span></th>
<th><span data-ttu-id="a39a8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a39a8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a39a8-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="a39a8-112">None</span></span></td>
<td><span data-ttu-id="a39a8-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="a39a8-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a39a8-114">NewKey</span><span class="sxs-lookup"><span data-stu-id="a39a8-114">NewKey</span></span></td>
<td><span data-ttu-id="a39a8-115">È necessario costruire una nuova chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a39a8-115">A new search key should be constructed.</span></span> <span data-ttu-id="a39a8-116">Qualsiasi chiave di ricerca precedentemente esistente viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="a39a8-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a39a8-117">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="a39a8-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="a39a8-118">Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate, qualsiasi chiave di ricerca già esistente viene eliminata e il contenuto del buffer di input viene caricato come nuova chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a39a8-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a39a8-119">KeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="a39a8-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="a39a8-120">Se la dimensione del buffer di input è zero e la colonna chiave corrente è una colonna a lunghezza variabile, questa opzione indica che il buffer di input contiene un valore di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="a39a8-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="a39a8-121">In caso contrario, una dimensione del buffer di input pari a zero indicherebbe un valore NULL.</span><span class="sxs-lookup"><span data-stu-id="a39a8-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a39a8-122">StrLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-122">StrLimit</span></span></td>
<td><span data-ttu-id="a39a8-123">Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a39a8-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="a39a8-125">Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che la colonna chiave corrente venga considerata come un carattere jolly di prefisso e che tutte le colonne chiave che preentrano nella colonna chiave corrente siano considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a39a8-126">FullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="a39a8-127">La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a39a8-128">FullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="a39a8-129">La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che si trovano dopo la colonna chiave corrente siano considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a39a8-130">PartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="a39a8-131">La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata come un carattere jolly di prefisso e che tutte le colonne chiave successive alla colonna chiave corrente siano considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a39a8-132">PartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="a39a8-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="a39a8-133">La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata come un carattere jolly di prefisso e che tutte le colonne chiave successive alla colonna chiave corrente siano considerate caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a39a8-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a39a8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a39a8-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a39a8-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a39a8-135">Reference</span></span>

[<span data-ttu-id="a39a8-136">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a39a8-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
