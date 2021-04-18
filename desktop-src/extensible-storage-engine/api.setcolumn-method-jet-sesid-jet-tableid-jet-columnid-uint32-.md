---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100879
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc3950db60b4d7fb52309e246555802f1624d6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316955"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint32"></a><span data-ttu-id="89dea-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span><span class="sxs-lookup"><span data-stu-id="89dea-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</span></span>

<span data-ttu-id="89dea-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="89dea-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="89dea-105">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="89dea-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="89dea-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89dea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89dea-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89dea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89dea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89dea-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As UIntegerApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    uint data
)
```

#### <a name="parameters"></a><span data-ttu-id="89dea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89dea-109">Parameters</span></span>

  - <span data-ttu-id="89dea-110">sesid</span><span class="sxs-lookup"><span data-stu-id="89dea-110">sesid</span></span>  
    <span data-ttu-id="89dea-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89dea-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="89dea-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="89dea-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="89dea-113">TableID</span><span class="sxs-lookup"><span data-stu-id="89dea-113">tableid</span></span>  
    <span data-ttu-id="89dea-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89dea-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="89dea-115">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="89dea-115">The cursor to update.</span></span> <span data-ttu-id="89dea-116">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="89dea-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="89dea-117">columnid</span><span class="sxs-lookup"><span data-stu-id="89dea-117">columnid</span></span>  
    <span data-ttu-id="89dea-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89dea-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="89dea-119">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="89dea-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="89dea-120">data</span><span class="sxs-lookup"><span data-stu-id="89dea-120">data</span></span>  
    <span data-ttu-id="89dea-121">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="89dea-121">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="89dea-122">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="89dea-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="89dea-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89dea-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89dea-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89dea-124">Reference</span></span>

[<span data-ttu-id="89dea-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="89dea-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="89dea-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="89dea-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="89dea-127">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="89dea-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="89dea-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89dea-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
