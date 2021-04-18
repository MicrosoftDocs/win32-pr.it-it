---
description: 'Altre informazioni su: campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault'
title: Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313070"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a><span data-ttu-id="e9920-103">Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="e9920-103">Server2003Grbits.EnumerateIgnoreUserDefinedDefault field</span></span>

<span data-ttu-id="e9920-104">Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="e9920-104">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="e9920-105">Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.</span><span class="sxs-lookup"><span data-stu-id="e9920-105">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span>

<span data-ttu-id="e9920-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9920-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="e9920-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9920-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9920-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9920-108">Syntax</span></span>

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a><span data-ttu-id="e9920-109">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e9920-109">Remarks</span></span>

<span data-ttu-id="e9920-110">Questa opzione è disponibile solo per i sistemi operativi Windows Server 2003 SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e9920-110">This option is only available for Windows Server 2003 SP1 and later operating systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9920-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9920-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9920-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e9920-112">Reference</span></span>

[<span data-ttu-id="e9920-113">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="e9920-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="e9920-114">Membri di Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="e9920-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="e9920-115">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="e9920-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
