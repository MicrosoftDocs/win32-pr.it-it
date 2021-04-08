---
description: 'Altre informazioni su: Proprietà JET_SPACEHINTS. ulGrowth'
title: Proprietà JET_SPACEHINTS. ulGrowth
TOCTitle: 'ulGrowth property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.ulgrowth(v=EXCHG.10)
ms:contentKeyID: 55103929
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.set_ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.get_ulGrowth
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 946975a1777778871ecb8ae66c8e567e7c2ffcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749762"
---
# <a name="jet_spacehintsulgrowth-property"></a><span data-ttu-id="5daea-103">Proprietà JET_SPACEHINTS. ulGrowth</span><span class="sxs-lookup"><span data-stu-id="5daea-103">JET_SPACEHINTS.ulGrowth property</span></span>

<span data-ttu-id="5daea-104">Ottiene o imposta la percentuale di crescita dall'ultima crescita o dalle dimensioni iniziali (probabilmente arrotondate alle dimensioni di allocazione del JET nativo più vicine).</span><span class="sxs-lookup"><span data-stu-id="5daea-104">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="5daea-105">I valori validi sono 0 e \[ 100, 50000).</span><span class="sxs-lookup"><span data-stu-id="5daea-105">Valid values are 0, and \[100, 50000).</span></span>

<span data-ttu-id="5daea-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5daea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5daea-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5daea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5daea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5daea-108">Syntax</span></span>

``` vb
'Declaration
Public Property ulGrowth As Integer
    Get
    Set
'Usage
Dim instance As JET_SPACEHINTS
Dim value As Integer

value = instance.ulGrowth

instance.ulGrowth = value
```

``` csharp
public int ulGrowth { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5daea-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5daea-109">Property value</span></span>

<span data-ttu-id="5daea-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5daea-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5daea-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5daea-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5daea-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5daea-112">Reference</span></span>

[<span data-ttu-id="5daea-113">Classe JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5daea-113">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="5daea-114">Membri JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5daea-114">JET_SPACEHINTS members</span></span>](./jet-spacehints-members.md)

[<span data-ttu-id="5daea-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5daea-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
