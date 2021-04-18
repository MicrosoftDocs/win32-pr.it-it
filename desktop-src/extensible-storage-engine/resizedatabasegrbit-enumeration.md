---
description: 'Altre informazioni su: Enumerazione ResizeDatabaseGrbit'
title: Enumerazione ResizeDatabaseGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313079"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="8dd0a-103">Enumerazione ResizeDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="8dd0a-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="8dd0a-104">Opzioni per [JetResizeDatabase (JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="8dd0a-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="8dd0a-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8dd0a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dd0a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8dd0a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dd0a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd0a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8dd0a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="8dd0a-109">Members</span><span class="sxs-lookup"><span data-stu-id="8dd0a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8dd0a-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="8dd0a-110">Member name</span></span></th>
<th><span data-ttu-id="8dd0a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd0a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dd0a-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="8dd0a-112">None</span></span></td>
<td><span data-ttu-id="8dd0a-113">Nessuna opzione.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8dd0a-114">OnlyGrow</span><span class="sxs-lookup"><span data-stu-id="8dd0a-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="8dd0a-115">Espandere solo il database.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-115">Only grow the database.</span></span> <span data-ttu-id="8dd0a-116">Se la chiamata di ridimensionamento riduce il database, non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8dd0a-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dd0a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dd0a-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8dd0a-118">Reference</span></span>

[<span data-ttu-id="8dd0a-119">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="8dd0a-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
