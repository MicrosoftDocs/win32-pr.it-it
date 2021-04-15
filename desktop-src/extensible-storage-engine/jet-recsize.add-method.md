---
description: 'Altre informazioni su: JET_RECSIZE. Aggiungi metodo'
title: JET_RECSIZE. Metodo Add (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.add(v=EXCHG.10)
ms:contentKeyID: 39509872
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e12a78a0a32bcca02afec100b0b238f4444a6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525021"
---
# <a name="jet_recsizeadd-method"></a><span data-ttu-id="7895e-103">JET_RECSIZE. Aggiungi metodo</span><span class="sxs-lookup"><span data-stu-id="7895e-103">JET_RECSIZE.Add method</span></span>

<span data-ttu-id="7895e-104">Aggiungere le dimensioni in due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="7895e-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="7895e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7895e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7895e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7895e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7895e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7895e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Add(s1, s2)
```

``` csharp
public static JET_RECSIZE Add(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="7895e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7895e-108">Parameters</span></span>

  - <span data-ttu-id="7895e-109">s1</span><span class="sxs-lookup"><span data-stu-id="7895e-109">s1</span></span>  
    <span data-ttu-id="7895e-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7895e-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="7895e-111">Primo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="7895e-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="7895e-112">s2</span><span class="sxs-lookup"><span data-stu-id="7895e-112">s2</span></span>  
    <span data-ttu-id="7895e-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7895e-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="7895e-114">Secondo JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="7895e-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7895e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7895e-115">Return value</span></span>

<span data-ttu-id="7895e-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7895e-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="7895e-117">JET_RECSIZE contenente il risultato dell'aggiunta delle dimensioni in S1 e S2.</span><span class="sxs-lookup"><span data-stu-id="7895e-117">A JET_RECSIZE containing the result of adding the sizes in s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7895e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7895e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7895e-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7895e-119">Reference</span></span>

[<span data-ttu-id="7895e-120">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7895e-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="7895e-121">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7895e-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="7895e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="7895e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
