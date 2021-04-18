---
description: 'Altre informazioni su: Enumerazione SetCurrentIndexGrbit'
title: Enumerazione SetCurrentIndexGrbit
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308015"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="0057c-103">Enumerazione SetCurrentIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="0057c-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="0057c-104">Opzioni per [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) e [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="0057c-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="0057c-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="0057c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0057c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0057c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0057c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0057c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0057c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0057c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="0057c-109">Members</span><span class="sxs-lookup"><span data-stu-id="0057c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0057c-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="0057c-110">Member name</span></span></th>
<th><span data-ttu-id="0057c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0057c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0057c-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="0057c-112">None</span></span></td>
<td><span data-ttu-id="0057c-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="0057c-113">Default options.</span></span> <span data-ttu-id="0057c-114">Corrisponde a MoveFirst.</span><span class="sxs-lookup"><span data-stu-id="0057c-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0057c-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="0057c-115">MoveFirst</span></span></td>
<td><span data-ttu-id="0057c-116">Indica che il cursore deve essere posizionato sulla prima voce dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0057c-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="0057c-117">Se viene selezionato l'indice corrente, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0057c-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0057c-118">Nomove</span><span class="sxs-lookup"><span data-stu-id="0057c-118">NoMove</span></span></td>
<td><span data-ttu-id="0057c-119">Indica che il cursore deve essere posizionato sulla voce di indice del nuovo indice che corrisponde al record associato alla voce di indice in corrispondenza della posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="0057c-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0057c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0057c-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0057c-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0057c-121">Reference</span></span>

[<span data-ttu-id="0057c-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0057c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
