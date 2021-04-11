---
description: 'Altre informazioni su: metodo API. JetComputeStats'
title: API. JetComputeStats, metodo
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225854"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="2633f-103">API. JetComputeStats, metodo</span><span class="sxs-lookup"><span data-stu-id="2633f-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="2633f-104">Esamina ogni indice di una tabella per calcolare esattamente il numero di voci in un indice e il numero di chiavi distinte in un indice.</span><span class="sxs-lookup"><span data-stu-id="2633f-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="2633f-105">Queste informazioni, insieme al numero di pagine di database allocate per un indice e all'ora corrente del calcolo, vengono archiviate nei metadati dell'indice nel database.</span><span class="sxs-lookup"><span data-stu-id="2633f-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="2633f-106">Questi dati possono essere successivamente recuperati con le operazioni relative alle informazioni.</span><span class="sxs-lookup"><span data-stu-id="2633f-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="2633f-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2633f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2633f-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2633f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2633f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2633f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="2633f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2633f-110">Parameters</span></span>

  - <span data-ttu-id="2633f-111">sesid</span><span class="sxs-lookup"><span data-stu-id="2633f-111">sesid</span></span>  
    <span data-ttu-id="2633f-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2633f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2633f-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2633f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2633f-114">TableID</span><span class="sxs-lookup"><span data-stu-id="2633f-114">tableid</span></span>  
    <span data-ttu-id="2633f-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2633f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2633f-116">Tabella in cui verranno calcolate le statistiche.</span><span class="sxs-lookup"><span data-stu-id="2633f-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="2633f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2633f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2633f-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2633f-118">Reference</span></span>

[<span data-ttu-id="2633f-119">Classe API</span><span class="sxs-lookup"><span data-stu-id="2633f-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2633f-120">Membri API</span><span class="sxs-lookup"><span data-stu-id="2633f-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2633f-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2633f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
