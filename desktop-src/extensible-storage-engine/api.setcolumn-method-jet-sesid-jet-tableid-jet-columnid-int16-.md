---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int16)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100922
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
ms.openlocfilehash: 1f15c9b9340effdab5949d34c58393d3bc58a416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058175"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int16"></a><span data-ttu-id="b1675-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</span><span class="sxs-lookup"><span data-stu-id="b1675-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</span></span>

<span data-ttu-id="b1675-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="b1675-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="b1675-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1675-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1675-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1675-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1675-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1675-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Short _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As ShortApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    short data
)
```

#### <a name="parameters"></a><span data-ttu-id="b1675-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1675-108">Parameters</span></span>

  - <span data-ttu-id="b1675-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b1675-109">sesid</span></span>  
    <span data-ttu-id="b1675-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1675-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b1675-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b1675-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1675-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b1675-112">tableid</span></span>  
    <span data-ttu-id="b1675-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1675-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b1675-114">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b1675-114">The cursor to update.</span></span> <span data-ttu-id="b1675-115">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b1675-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1675-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b1675-116">columnid</span></span>  
    <span data-ttu-id="b1675-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b1675-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b1675-118">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="b1675-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1675-119">data</span><span class="sxs-lookup"><span data-stu-id="b1675-119">data</span></span>  
    <span data-ttu-id="b1675-120">Tipo: [System. Int16](/dotnet/api/system.int16)</span><span class="sxs-lookup"><span data-stu-id="b1675-120">Type: [System.Int16](/dotnet/api/system.int16)</span></span>  
    
    <span data-ttu-id="b1675-121">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="b1675-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1675-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1675-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1675-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b1675-123">Reference</span></span>

[<span data-ttu-id="b1675-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="b1675-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b1675-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="b1675-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b1675-126">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="b1675-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="b1675-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b1675-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
