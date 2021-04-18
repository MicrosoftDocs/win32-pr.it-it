---
description: 'Altre informazioni su: JET_RECSIZE. Metodo Subtract'
title: JET_RECSIZE. Metodo Subtract (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315646"
---
# <a name="jet_recsizesubtract-method"></a><span data-ttu-id="68ade-103">JET_RECSIZE. Metodo Subtract</span><span class="sxs-lookup"><span data-stu-id="68ade-103">JET_RECSIZE.Subtract method</span></span>

<span data-ttu-id="68ade-104">Calcolare la differenza di dimensioni tra due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="68ade-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="68ade-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68ade-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="68ade-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68ade-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68ade-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68ade-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="68ade-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68ade-108">Parameters</span></span>

  - <span data-ttu-id="68ade-109">s1</span><span class="sxs-lookup"><span data-stu-id="68ade-109">s1</span></span>  
    <span data-ttu-id="68ade-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="68ade-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="68ade-111">Primo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="68ade-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="68ade-112">s2</span><span class="sxs-lookup"><span data-stu-id="68ade-112">s2</span></span>  
    <span data-ttu-id="68ade-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="68ade-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="68ade-114">Secondo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="68ade-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68ade-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68ade-115">Return value</span></span>

<span data-ttu-id="68ade-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="68ade-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="68ade-117">JET_RECSIZE che contiene la differenza di dimensioni tra S1 e S2.</span><span class="sxs-lookup"><span data-stu-id="68ade-117">A JET_RECSIZE containing the difference in sizes between s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68ade-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68ade-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68ade-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="68ade-119">Reference</span></span>

[<span data-ttu-id="68ade-120">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="68ade-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="68ade-121">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="68ade-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="68ade-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="68ade-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
