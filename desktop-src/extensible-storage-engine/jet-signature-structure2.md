---
description: 'Altre informazioni su: struttura JET_SIGNATURE'
title: Struttura JET_SIGNATURE
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5c8ce12b23194aea2a45c273e0207f88faad6f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308022"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="f6768-103">Struttura JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="f6768-103">JET_SIGNATURE structure</span></span>

<span data-ttu-id="f6768-104">La struttura JET_SIGNATURE contiene informazioni che identificano in modo univoco una sequenza di database o logfile.</span><span class="sxs-lookup"><span data-stu-id="f6768-104">The JET_SIGNATURE structure contains information that uniquely identifies a database or logfile sequence.</span></span>

<span data-ttu-id="f6768-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6768-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6768-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6768-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6768-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6768-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a><span data-ttu-id="f6768-108">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f6768-108">Thread safety</span></span>

<span data-ttu-id="f6768-109">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f6768-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f6768-110">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f6768-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6768-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6768-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6768-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f6768-112">Reference</span></span>

[<span data-ttu-id="f6768-113">Membri JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="f6768-113">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="f6768-114">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f6768-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
