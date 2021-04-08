---
description: 'Altre informazioni su: Proprietà JET_RETRIEVECOLUMN. cbData'
title: Proprietà JET_RETRIEVECOLUMN. cbData
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b91e78d31e2c82b0825da5e320fef558f790caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752479"
---
# <a name="jet_retrievecolumncbdata-property"></a><span data-ttu-id="c0d2a-103">Proprietà JET_RETRIEVECOLUMN. cbData</span><span class="sxs-lookup"><span data-stu-id="c0d2a-103">JET_RETRIEVECOLUMN.cbData property</span></span>

<span data-ttu-id="c0d2a-104">Ottiene o imposta le dimensioni in byte del buffer [pvData](./jet-retrievecolumn.pvdata-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d2a-104">Gets or sets the size of the [pvData](./jet-retrievecolumn.pvdata-property.md) buffer, in bytes.</span></span> <span data-ttu-id="c0d2a-105">Tramite l'operazione di recupero colonna non vengono archiviati più dati in pvData rispetto a cbData.</span><span class="sxs-lookup"><span data-stu-id="c0d2a-105">The retrieve column operation will not store more data in pvData than cbData.</span></span>

<span data-ttu-id="c0d2a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0d2a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0d2a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c0d2a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d2a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0d2a-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.cbData

instance.cbData = value
```

``` csharp
public int cbData { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c0d2a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c0d2a-109">Property value</span></span>

<span data-ttu-id="c0d2a-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c0d2a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0d2a-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0d2a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0d2a-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c0d2a-112">Reference</span></span>

[<span data-ttu-id="c0d2a-113">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="c0d2a-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="c0d2a-114">Membri JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="c0d2a-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="c0d2a-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c0d2a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
