---
description: 'Altre informazioni su: JET_RECSIZE. Operatore di addizione'
title: JET_RECSIZE. Operatore di addizione (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749826"
---
# <a name="jet_recsizeaddition-operator"></a><span data-ttu-id="78a05-103">JET_RECSIZE. Operatore di addizione</span><span class="sxs-lookup"><span data-stu-id="78a05-103">JET_RECSIZE.Addition operator</span></span>

<span data-ttu-id="78a05-104">Aggiungere le dimensioni in due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="78a05-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="78a05-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78a05-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="78a05-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78a05-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78a05-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78a05-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="78a05-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78a05-108">Parameters</span></span>

  - <span data-ttu-id="78a05-109">sinistro</span><span class="sxs-lookup"><span data-stu-id="78a05-109">left</span></span>  
    <span data-ttu-id="78a05-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="78a05-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="78a05-111">Primo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="78a05-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="78a05-112">right</span><span class="sxs-lookup"><span data-stu-id="78a05-112">right</span></span>  
    <span data-ttu-id="78a05-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="78a05-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="78a05-114">Secondo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="78a05-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="78a05-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78a05-115">Return value</span></span>

<span data-ttu-id="78a05-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="78a05-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="78a05-117">JET_RECSIZE contenente il risultato dell'aggiunta delle dimensioni a sinistra e a destra.</span><span class="sxs-lookup"><span data-stu-id="78a05-117">A JET_RECSIZE containing the result of adding the sizes in left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78a05-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78a05-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78a05-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="78a05-119">Reference</span></span>

[<span data-ttu-id="78a05-120">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="78a05-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="78a05-121">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="78a05-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="78a05-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="78a05-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
