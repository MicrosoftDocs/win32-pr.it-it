---
description: 'Altre informazioni su: Proprietà JET_RETINFO. itagSequence'
title: Proprietà JET_RETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233640"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="1e278-103">Proprietà JET_RETINFO. itagSequence</span><span class="sxs-lookup"><span data-stu-id="1e278-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="1e278-104">Ottiene o imposta il numero di sequenza del valore in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="1e278-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="1e278-105">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="1e278-105">The array of values is one-based.</span></span> <span data-ttu-id="1e278-106">Il primo valore è Sequence 1, not 0.</span><span class="sxs-lookup"><span data-stu-id="1e278-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="1e278-107">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence.</span><span class="sxs-lookup"><span data-stu-id="1e278-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="1e278-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1e278-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1e278-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1e278-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1e278-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e278-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1e278-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1e278-111">Property value</span></span>

<span data-ttu-id="1e278-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1e278-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e278-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e278-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1e278-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1e278-114">Reference</span></span>

[<span data-ttu-id="1e278-115">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="1e278-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="1e278-116">Membri JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="1e278-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="1e278-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1e278-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
