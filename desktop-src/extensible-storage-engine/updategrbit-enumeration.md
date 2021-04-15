---
description: 'Altre informazioni su: Enumerazione UpdateGrbit'
title: Enumerazione UpdateGrbit (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526791"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="b1ff2-103">Enumerazione UpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="b1ff2-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="b1ff2-104">Opzioni per [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span><span class="sxs-lookup"><span data-stu-id="b1ff2-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="b1ff2-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="b1ff2-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b1ff2-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1ff2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="b1ff2-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1ff2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ff2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1ff2-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="b1ff2-109">Members</span><span class="sxs-lookup"><span data-stu-id="b1ff2-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b1ff2-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="b1ff2-110">Member name</span></span></th>
<th><span data-ttu-id="b1ff2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1ff2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b1ff2-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="b1ff2-112">None</span></span></td>
<td><span data-ttu-id="b1ff2-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="b1ff2-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b1ff2-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="b1ff2-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="b1ff2-115"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="b1ff2-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="b1ff2-116">Questo flag fa in modo che l'aggiornamento restituisca un errore se l'aggiornamento non è stato possibile nella versione Windows 2000 di ESE, che ha applicato un numero massimo di istanze di colonna multivalore inferiore in ogni record rispetto alle versioni successive di ESE.</span><span class="sxs-lookup"><span data-stu-id="b1ff2-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="b1ff2-117">Questo aspetto è importante solo per le applicazioni che vogliono replicare i dati tra le applicazioni ospitate in Windows 2000 e le applicazioni ospitate in Windows 2003 o versioni successive di ESE.</span><span class="sxs-lookup"><span data-stu-id="b1ff2-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="b1ff2-118">Non dovrebbe essere necessario per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b1ff2-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b1ff2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1ff2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1ff2-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b1ff2-120">Reference</span></span>

[<span data-ttu-id="b1ff2-121">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="b1ff2-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
