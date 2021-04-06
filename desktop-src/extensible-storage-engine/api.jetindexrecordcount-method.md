---
description: 'Altre informazioni su: metodo API. JetIndexRecordCount'
title: API. JetIndexRecordCount, metodo
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759428"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="03a9a-103">API. JetIndexRecordCount, metodo</span><span class="sxs-lookup"><span data-stu-id="03a9a-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="03a9a-104">Conta il numero di voci nell'indice corrente dalla posizione corrente in poi.</span><span class="sxs-lookup"><span data-stu-id="03a9a-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="03a9a-105">La posizione corrente è inclusa nel conteggio.</span><span class="sxs-lookup"><span data-stu-id="03a9a-105">The current position is included in the count.</span></span> <span data-ttu-id="03a9a-106">Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente è su una colonna multivalore e le istanze della colonna hanno più valori.</span><span class="sxs-lookup"><span data-stu-id="03a9a-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="03a9a-107">Se la tabella è vuota, verrà restituito 0 per il conteggio.</span><span class="sxs-lookup"><span data-stu-id="03a9a-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="03a9a-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="03a9a-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="03a9a-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="03a9a-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="03a9a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03a9a-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="03a9a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="03a9a-111">Parameters</span></span>

  - <span data-ttu-id="03a9a-112">sesid</span><span class="sxs-lookup"><span data-stu-id="03a9a-112">sesid</span></span>  
    <span data-ttu-id="03a9a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="03a9a-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="03a9a-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="03a9a-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="03a9a-115">TableID</span><span class="sxs-lookup"><span data-stu-id="03a9a-115">tableid</span></span>  
    <span data-ttu-id="03a9a-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="03a9a-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="03a9a-117">Cursore in cui conteggiare i record.</span><span class="sxs-lookup"><span data-stu-id="03a9a-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="03a9a-118">numRecords</span><span class="sxs-lookup"><span data-stu-id="03a9a-118">numRecords</span></span>  
    <span data-ttu-id="03a9a-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="03a9a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="03a9a-120">Restituisce il numero di record.</span><span class="sxs-lookup"><span data-stu-id="03a9a-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="03a9a-121">maxRecordsToCount</span><span class="sxs-lookup"><span data-stu-id="03a9a-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="03a9a-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="03a9a-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="03a9a-123">Numero massimo di record da contare.</span><span class="sxs-lookup"><span data-stu-id="03a9a-123">The maximum number of records to count.</span></span> <span data-ttu-id="03a9a-124">Il valore 0 indica che il conteggio è illimitato.</span><span class="sxs-lookup"><span data-stu-id="03a9a-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="03a9a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03a9a-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03a9a-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="03a9a-126">Reference</span></span>

[<span data-ttu-id="03a9a-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="03a9a-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="03a9a-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="03a9a-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="03a9a-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="03a9a-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
