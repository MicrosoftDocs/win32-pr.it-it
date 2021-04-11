---
description: 'Altre informazioni su: Proprietà JET_SETINFO. itagSequence'
title: Proprietà JET_SETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128642"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="e5ab0-103">Proprietà JET_SETINFO. itagSequence</span><span class="sxs-lookup"><span data-stu-id="e5ab0-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="e5ab0-104">Ottiene o imposta il numero di sequenza del valore in una colonna multivalore da impostare.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="e5ab0-105">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-105">The array of values is one-based.</span></span> <span data-ttu-id="e5ab0-106">Il primo valore è Sequence 1, non 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e5ab0-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="e5ab0-107">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence se tale valore viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="e5ab0-108">Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="e5ab0-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5ab0-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5ab0-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5ab0-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ab0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5ab0-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e5ab0-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e5ab0-112">Property value</span></span>

<span data-ttu-id="e5ab0-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e5ab0-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5ab0-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5ab0-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5ab0-115">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e5ab0-115">Reference</span></span>

[<span data-ttu-id="e5ab0-116">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e5ab0-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="e5ab0-117">Membri JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e5ab0-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="e5ab0-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e5ab0-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
