---
description: 'Altre informazioni su: Enumerazione LsGrbit'
title: Enumerazione LsGrbit
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049553"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="c4341-103">Enumerazione LsGrbit</span><span class="sxs-lookup"><span data-stu-id="c4341-103">LsGrbit enumeration</span></span>

<span data-ttu-id="c4341-104">Opzioni per [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) e [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="c4341-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="c4341-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="c4341-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c4341-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4341-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4341-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c4341-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4341-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4341-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="c4341-109">Members</span><span class="sxs-lookup"><span data-stu-id="c4341-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c4341-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="c4341-110">Member name</span></span></th>
<th><span data-ttu-id="c4341-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4341-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c4341-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="c4341-112">None</span></span></td>
<td><span data-ttu-id="c4341-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="c4341-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c4341-114">Reset</span><span class="sxs-lookup"><span data-stu-id="c4341-114">Reset</span></span></td>
<td><span data-ttu-id="c4341-115">L'handle del contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="c4341-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c4341-116">Cursore</span><span class="sxs-lookup"><span data-stu-id="c4341-116">Cursor</span></span></td>
<td><span data-ttu-id="c4341-117">Specifica che l'handle di contesto deve essere associato al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="c4341-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c4341-118">Tabella</span><span class="sxs-lookup"><span data-stu-id="c4341-118">Table</span></span></td>
<td><span data-ttu-id="c4341-119">Specifica che l'handle di contesto deve essere associato alla tabella associata al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="c4341-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="c4341-120">Non è consentito utilizzare questa opzione con Cursor.</span><span class="sxs-lookup"><span data-stu-id="c4341-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c4341-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4341-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4341-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c4341-122">Reference</span></span>

[<span data-ttu-id="c4341-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c4341-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
