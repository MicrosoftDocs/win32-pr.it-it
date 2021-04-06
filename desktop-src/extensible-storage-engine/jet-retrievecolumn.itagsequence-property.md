---
description: 'Altre informazioni su: Proprietà JET_RETRIEVECOLUMN. itagSequence'
title: Proprietà JET_RETRIEVECOLUMN. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103882
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f2885d5bf467d282ef97172323a8de44980ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883781"
---
# <a name="jet_retrievecolumnitagsequence-property"></a><span data-ttu-id="61afa-103">Proprietà JET_RETRIEVECOLUMN. itagSequence</span><span class="sxs-lookup"><span data-stu-id="61afa-103">JET_RETRIEVECOLUMN.itagSequence property</span></span>

<span data-ttu-id="61afa-104">Ottiene o imposta il numero di sequenza dei valori contenuti in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="61afa-104">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="61afa-105">Se itagSequence è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="61afa-105">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span>

<span data-ttu-id="61afa-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61afa-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61afa-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61afa-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61afa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61afa-108">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="61afa-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="61afa-109">Property value</span></span>

<span data-ttu-id="61afa-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61afa-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="61afa-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61afa-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61afa-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="61afa-112">Reference</span></span>

[<span data-ttu-id="61afa-113">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="61afa-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="61afa-114">Membri JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="61afa-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="61afa-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="61afa-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
