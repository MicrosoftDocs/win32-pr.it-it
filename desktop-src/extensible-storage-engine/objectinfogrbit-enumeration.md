---
description: 'Altre informazioni su: Enumerazione ObjectInfoGrbit'
title: Enumerazione ObjectInfoGrbit
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313090"
---
# <a name="objectinfogrbit-enumeration"></a><span data-ttu-id="d0ffc-103">Enumerazione ObjectInfoGrbit</span><span class="sxs-lookup"><span data-stu-id="d0ffc-103">ObjectInfoGrbit enumeration</span></span>

<span data-ttu-id="d0ffc-104">Opzioni tabella, utilizzate in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="d0ffc-104">Table options, used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="d0ffc-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d0ffc-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0ffc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0ffc-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0ffc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ffc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0ffc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
```

## <a name="members"></a><span data-ttu-id="d0ffc-109">Members</span><span class="sxs-lookup"><span data-stu-id="d0ffc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d0ffc-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d0ffc-110">Member name</span></span></th>
<th><span data-ttu-id="d0ffc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0ffc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d0ffc-112">Segnalibro</span><span class="sxs-lookup"><span data-stu-id="d0ffc-112">Bookmark</span></span></td>
<td><span data-ttu-id="d0ffc-113">La tabella può includere segnalibri.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-113">The table can have bookmarks.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d0ffc-114">Rollback</span><span class="sxs-lookup"><span data-stu-id="d0ffc-114">Rollback</span></span></td>
<td><span data-ttu-id="d0ffc-115">È possibile eseguire il rollback della tabella.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-115">The table can be rolled back.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d0ffc-116">Aggiornabile</span><span class="sxs-lookup"><span data-stu-id="d0ffc-116">Updatable</span></span></td>
<td><span data-ttu-id="d0ffc-117">È possibile aggiornare la tabella.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-117">The table can be updated.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d0ffc-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0ffc-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0ffc-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d0ffc-119">Reference</span></span>

[<span data-ttu-id="d0ffc-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0ffc-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
