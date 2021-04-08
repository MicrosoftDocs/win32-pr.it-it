---
description: 'Altre informazioni su: Enumerazione MoveGrbit'
title: Enumerazione MoveGrbit
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050107"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="720d4-103">Enumerazione MoveGrbit</span><span class="sxs-lookup"><span data-stu-id="720d4-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="720d4-104">Opzioni per JetMove.</span><span class="sxs-lookup"><span data-stu-id="720d4-104">Options for JetMove.</span></span>

<span data-ttu-id="720d4-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="720d4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="720d4-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="720d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="720d4-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="720d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="720d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="720d4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="720d4-109">Members</span><span class="sxs-lookup"><span data-stu-id="720d4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="720d4-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="720d4-110">Member name</span></span></th>
<th><span data-ttu-id="720d4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720d4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="720d4-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="720d4-112">None</span></span></td>
<td><span data-ttu-id="720d4-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="720d4-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="720d4-114">MoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="720d4-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="720d4-115">Sposta il cursore avanti o indietro per il numero di voci di indice necessarie per ignorare il numero richiesto di valori di chiave di indice rilevati nell'indice.</span><span class="sxs-lookup"><span data-stu-id="720d4-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="720d4-116">Questo ha l'effetto di comprimere le voci di indice con valori di chiave duplicati in una singola voce di indice.</span><span class="sxs-lookup"><span data-stu-id="720d4-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="720d4-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="720d4-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="720d4-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="720d4-118">Reference</span></span>

[<span data-ttu-id="720d4-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="720d4-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
