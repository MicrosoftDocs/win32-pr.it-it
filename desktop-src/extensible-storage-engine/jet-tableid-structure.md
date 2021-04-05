---
description: 'Altre informazioni su: struttura JET_TABLEID'
title: Struttura JET_TABLEID
TOCTitle: JET_TABLEID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid(v=EXCHG.10)
ms:contentKeyID: 39516503
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72713007ace7fb93b3f01ec8e5fc25cbe127298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058001"
---
# <a name="jet_tableid-structure"></a><span data-ttu-id="86a6a-103">Struttura JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="86a6a-103">JET_TABLEID structure</span></span>

<span data-ttu-id="86a6a-104">Un JET_TABLEID contiene un handle per il cursore del database da usare per una chiamata all'API JET.</span><span class="sxs-lookup"><span data-stu-id="86a6a-104">A JET_TABLEID contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="86a6a-105">Un cursore può essere utilizzato solo con la sessione utilizzata per aprire il cursore.</span><span class="sxs-lookup"><span data-stu-id="86a6a-105">A cursor can only be used with the session that was used to open that cursor.</span></span>

<span data-ttu-id="86a6a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="86a6a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="86a6a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="86a6a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="86a6a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86a6a-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_TABLEID _
    Implements IEquatable(Of JET_TABLEID), IFormattable
'Usage
Dim instance As JET_TABLEID
```

``` csharp
public struct JET_TABLEID : IEquatable<JET_TABLEID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="86a6a-109">Thread safety</span><span class="sxs-lookup"><span data-stu-id="86a6a-109">Thread safety</span></span>

<span data-ttu-id="86a6a-110">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="86a6a-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="86a6a-111">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="86a6a-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="86a6a-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86a6a-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="86a6a-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="86a6a-113">Reference</span></span>

[<span data-ttu-id="86a6a-114">Membri JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="86a6a-114">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="86a6a-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="86a6a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
