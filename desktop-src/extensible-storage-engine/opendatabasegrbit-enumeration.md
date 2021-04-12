---
description: 'Altre informazioni su: Enumerazione OpenDatabaseGrbit'
title: Enumerazione OpenDatabaseGrbit
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231796"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="a0bc8-103">Enumerazione OpenDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="a0bc8-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="a0bc8-104">Opzioni per [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0bc8-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="a0bc8-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="a0bc8-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a0bc8-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0bc8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0bc8-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a0bc8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bc8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0bc8-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="a0bc8-109">Members</span><span class="sxs-lookup"><span data-stu-id="a0bc8-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a0bc8-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="a0bc8-110">Member name</span></span></th>
<th><span data-ttu-id="a0bc8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0bc8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a0bc8-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="a0bc8-112">None</span></span></td>
<td><span data-ttu-id="a0bc8-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="a0bc8-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a0bc8-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a0bc8-114">ReadOnly</span></span></td>
<td><span data-ttu-id="a0bc8-115">Impedisce le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="a0bc8-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a0bc8-116">Esclusivo</span><span class="sxs-lookup"><span data-stu-id="a0bc8-116">Exclusive</span></span></td>
<td><span data-ttu-id="a0bc8-117">Consente la connessione di un database a una singola sessione.</span><span class="sxs-lookup"><span data-stu-id="a0bc8-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="a0bc8-118">In genere, diverse sessioni possono aprire un database.</span><span class="sxs-lookup"><span data-stu-id="a0bc8-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a0bc8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0bc8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0bc8-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a0bc8-120">Reference</span></span>

[<span data-ttu-id="a0bc8-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a0bc8-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
