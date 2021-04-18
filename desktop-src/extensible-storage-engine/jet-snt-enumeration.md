---
description: 'Altre informazioni su: Enumerazione JET_SNT'
title: Enumerazione JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305762"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="d6ac1-103">Enumerazione JET_SNT</span><span class="sxs-lookup"><span data-stu-id="d6ac1-103">JET_SNT enumeration</span></span>

<span data-ttu-id="d6ac1-104">Tipo di stato di avanzamento segnalato.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-104">Type of progress being reported.</span></span>

<span data-ttu-id="d6ac1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6ac1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6ac1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6ac1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ac1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6ac1-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="d6ac1-108">Members</span><span class="sxs-lookup"><span data-stu-id="d6ac1-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d6ac1-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d6ac1-109">Member name</span></span></th>
<th><span data-ttu-id="d6ac1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6ac1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d6ac1-111">Inizia</span><span class="sxs-lookup"><span data-stu-id="d6ac1-111">Begin</span></span></td>
<td><span data-ttu-id="d6ac1-112">Callback per l'inizio di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d6ac1-113">Avanzamento</span><span class="sxs-lookup"><span data-stu-id="d6ac1-113">Progress</span></span></td>
<td><span data-ttu-id="d6ac1-114">Callback per lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d6ac1-115">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="d6ac1-115">Complete</span></span></td>
<td><span data-ttu-id="d6ac1-116">Callback per il completamento di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d6ac1-117">Esito negativo</span><span class="sxs-lookup"><span data-stu-id="d6ac1-117">Fail</span></span></td>
<td><span data-ttu-id="d6ac1-118">Callback per l'errore durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d6ac1-119">RecoveryStep</span><span class="sxs-lookup"><span data-stu-id="d6ac1-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="d6ac1-120">Callback per il controllo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="d6ac1-121">Usato per l'elaborazione interna nelle versioni del sistema operativo Windows precedenti a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="d6ac1-122">Questo valore non è applicabile alle versioni di Windows a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6ac1-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d6ac1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6ac1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6ac1-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d6ac1-124">Reference</span></span>

[<span data-ttu-id="d6ac1-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6ac1-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
