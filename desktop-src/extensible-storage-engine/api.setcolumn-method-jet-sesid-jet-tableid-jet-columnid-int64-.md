---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100926
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925d8483a799a23bc6551e6d3d13731c7f1f392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316956"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int64"></a><span data-ttu-id="1fa56-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</span><span class="sxs-lookup"><span data-stu-id="1fa56-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</span></span>

<span data-ttu-id="1fa56-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="1fa56-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="1fa56-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fa56-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fa56-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fa56-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa56-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fa56-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Long _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As LongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    long data
)
```

#### <a name="parameters"></a><span data-ttu-id="1fa56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fa56-108">Parameters</span></span>

  - <span data-ttu-id="1fa56-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1fa56-109">sesid</span></span>  
    <span data-ttu-id="1fa56-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fa56-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1fa56-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1fa56-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa56-112">TableID</span><span class="sxs-lookup"><span data-stu-id="1fa56-112">tableid</span></span>  
    <span data-ttu-id="1fa56-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fa56-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1fa56-114">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1fa56-114">The cursor to update.</span></span> <span data-ttu-id="1fa56-115">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1fa56-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa56-116">columnid</span><span class="sxs-lookup"><span data-stu-id="1fa56-116">columnid</span></span>  
    <span data-ttu-id="1fa56-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fa56-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1fa56-118">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="1fa56-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa56-119">data</span><span class="sxs-lookup"><span data-stu-id="1fa56-119">data</span></span>  
    <span data-ttu-id="1fa56-120">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="1fa56-120">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="1fa56-121">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="1fa56-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa56-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fa56-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fa56-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1fa56-123">Reference</span></span>

[<span data-ttu-id="1fa56-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="1fa56-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1fa56-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="1fa56-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1fa56-126">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="1fa56-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="1fa56-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1fa56-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
