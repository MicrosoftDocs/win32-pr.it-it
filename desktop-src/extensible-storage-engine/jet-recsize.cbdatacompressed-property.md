---
description: 'Altre informazioni su: Proprietà JET_RECSIZE. cbDataCompressed'
title: Proprietà JET_RECSIZE. cbDataCompressed (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749823"
---
# <a name="jet_recsizecbdatacompressed-property"></a><span data-ttu-id="4fc7d-103">Proprietà JET_RECSIZE. cbDataCompressed</span><span class="sxs-lookup"><span data-stu-id="4fc7d-103">JET_RECSIZE.cbDataCompressed property</span></span>

<span data-ttu-id="4fc7d-104">Ottiene la dimensione compressa dei dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="4fc7d-104">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="4fc7d-105">Si tratta dello stesso valore di [cbData](./jet-recsize.cbdata-property.md) se non vengono compressi valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="4fc7d-105">This is the same as [cbData](./jet-recsize.cbdata-property.md) if no intrinsic long-values are compressed).</span></span>

<span data-ttu-id="4fc7d-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fc7d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4fc7d-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4fc7d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc7d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fc7d-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="4fc7d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4fc7d-109">Property value</span></span>

<span data-ttu-id="4fc7d-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="4fc7d-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fc7d-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fc7d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fc7d-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4fc7d-112">Reference</span></span>

[<span data-ttu-id="4fc7d-113">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="4fc7d-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="4fc7d-114">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="4fc7d-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="4fc7d-115">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="4fc7d-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
