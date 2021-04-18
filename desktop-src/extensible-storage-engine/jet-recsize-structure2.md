---
description: 'Altre informazioni su: struttura JET_RECSIZE'
title: Struttura JET_RECSIZE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_RECSIZE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize(v=EXCHG.10)
ms:contentKeyID: 39509765
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e741d91187a138d7b8d9a57d0c4e76f54979d99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305782"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="855c3-103">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="855c3-103">JET_RECSIZE structure</span></span>

<span data-ttu-id="855c3-104">Utilizzato da [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, il numero di colonne set, il numero di valori e lo spazio overhead della struttura del record esent.</span><span class="sxs-lookup"><span data-stu-id="855c3-104">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="855c3-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="855c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="855c3-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="855c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="855c3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="855c3-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_RECSIZE _
    Implements IEquatable(Of JET_RECSIZE)
'Usage
Dim instance As JET_RECSIZE
```

``` csharp
[SerializableAttribute]
public struct JET_RECSIZE : IEquatable<JET_RECSIZE>
```

## <a name="thread-safety"></a><span data-ttu-id="855c3-108">Thread safety</span><span class="sxs-lookup"><span data-stu-id="855c3-108">Thread safety</span></span>

<span data-ttu-id="855c3-109">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="855c3-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="855c3-110">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="855c3-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="855c3-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="855c3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="855c3-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="855c3-112">Reference</span></span>

[<span data-ttu-id="855c3-113">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="855c3-113">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="855c3-114">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="855c3-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
