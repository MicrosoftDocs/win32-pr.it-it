---
description: 'Altre informazioni su: struttura JET_INDEXID'
title: Struttura JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318129"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="7d81c-103">Struttura JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="7d81c-103">JET_INDEXID structure</span></span>

<span data-ttu-id="7d81c-104">Include un ID di indice.</span><span class="sxs-lookup"><span data-stu-id="7d81c-104">Holds an index ID.</span></span> <span data-ttu-id="7d81c-105">Un ID di indice è un hint usato per accelerare la selezione dell'indice corrente usando JetSetCurrentIndex.</span><span class="sxs-lookup"><span data-stu-id="7d81c-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="7d81c-106">Risulta particolarmente utile quando è presente un numero molto elevato di indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="7d81c-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="7d81c-107">L'ID di indice può essere recuperato tramite JetGetIndexInfo o JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="7d81c-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="7d81c-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d81c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d81c-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d81c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d81c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d81c-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="7d81c-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7d81c-111">Remarks</span></span>

<span data-ttu-id="7d81c-112">L'attributo Pack è necessario perché la versione di C++ è definita come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="7d81c-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="7d81c-113">Se il \# compilatore C inserisce la spaziatura interna consueta tra uint cbStruct e IntPtr, la struttura è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="7d81c-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="7d81c-114">Thread safety</span><span class="sxs-lookup"><span data-stu-id="7d81c-114">Thread safety</span></span>

<span data-ttu-id="7d81c-115">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7d81c-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d81c-116">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7d81c-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d81c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d81c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d81c-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7d81c-118">Reference</span></span>

[<span data-ttu-id="7d81c-119">Membri JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="7d81c-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="7d81c-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7d81c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
