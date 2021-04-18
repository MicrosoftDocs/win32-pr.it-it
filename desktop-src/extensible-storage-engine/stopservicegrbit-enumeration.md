---
description: 'Altre informazioni su: Enumerazione StopServiceGrbit'
title: Enumerazione StopServiceGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308005"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="ea6f9-103">Enumerazione StopServiceGrbit</span><span class="sxs-lookup"><span data-stu-id="ea6f9-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="ea6f9-104">Opzioni per [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="ea6f9-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="ea6f9-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ea6f9-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ea6f9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="ea6f9-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ea6f9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6f9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea6f9-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="ea6f9-109">Members</span><span class="sxs-lookup"><span data-stu-id="ea6f9-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ea6f9-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="ea6f9-110">Member name</span></span></th>
<th><span data-ttu-id="ea6f9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea6f9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ea6f9-112">Tutti</span><span class="sxs-lookup"><span data-stu-id="ea6f9-112">All</span></span></td>
<td><span data-ttu-id="ea6f9-113">Arresta tutti i servizi ESE per l'istanza specificata.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ea6f9-114">BackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="ea6f9-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="ea6f9-115">Arresta le attività di manutenzione in background specifiche del client riavviabili (B + deframmentazione albero).</span><span class="sxs-lookup"><span data-stu-id="ea6f9-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ea6f9-116">QuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="ea6f9-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="ea6f9-117">Quiesces tutte le cache Dirty sul disco.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="ea6f9-118">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-118">Asynchronous.</span></span> <span data-ttu-id="ea6f9-119">Disattivazione viene annullato se il bit Resume viene chiamato successivamente.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ea6f9-120">Riprendi</span><span class="sxs-lookup"><span data-stu-id="ea6f9-120">Resume</span></span></td>
<td><span data-ttu-id="ea6f9-121">Riprende le operazioni StopService rilasciate in precedenza, ovvero &quot; Riavvia il servizio &quot; .</span><span class="sxs-lookup"><span data-stu-id="ea6f9-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="ea6f9-122">Può essere combinato con grbits sopra per riprendere servizi specifici o con 0x0 riprende tutti i servizi precedenti arrestati.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="ea6f9-123">Avviso: questo bit può essere utilizzato solo per riprendere JET_bitStopServiceBackground e JET_bitStopServiceQuiesceCaches, se è stato eseguito un JET_bitStopServiceAll o JET_bitStopServiceAPI, il tentativo di utilizzare JET_bitStopServiceResume avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ea6f9-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ea6f9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea6f9-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ea6f9-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ea6f9-125">Reference</span></span>

[<span data-ttu-id="ea6f9-126">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="ea6f9-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
