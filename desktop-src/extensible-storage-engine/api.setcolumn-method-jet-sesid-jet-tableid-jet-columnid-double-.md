---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100921
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
ms.openlocfilehash: 4a3d47b42e08a524a20d337abc40da974866ba1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319281"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-double"></a><span data-ttu-id="09b44-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</span><span class="sxs-lookup"><span data-stu-id="09b44-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</span></span>

<span data-ttu-id="09b44-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="09b44-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="09b44-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09b44-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09b44-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09b44-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09b44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09b44-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Double _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DoubleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    double data
)
```

#### <a name="parameters"></a><span data-ttu-id="09b44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09b44-108">Parameters</span></span>

  - <span data-ttu-id="09b44-109">sesid</span><span class="sxs-lookup"><span data-stu-id="09b44-109">sesid</span></span>  
    <span data-ttu-id="09b44-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09b44-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="09b44-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="09b44-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09b44-112">TableID</span><span class="sxs-lookup"><span data-stu-id="09b44-112">tableid</span></span>  
    <span data-ttu-id="09b44-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09b44-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="09b44-114">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="09b44-114">The cursor to update.</span></span> <span data-ttu-id="09b44-115">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="09b44-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="09b44-116">columnid</span><span class="sxs-lookup"><span data-stu-id="09b44-116">columnid</span></span>  
    <span data-ttu-id="09b44-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09b44-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="09b44-118">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="09b44-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="09b44-119">data</span><span class="sxs-lookup"><span data-stu-id="09b44-119">data</span></span>  
    <span data-ttu-id="09b44-120">Tipo: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="09b44-120">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="09b44-121">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="09b44-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="09b44-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09b44-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09b44-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="09b44-123">Reference</span></span>

[<span data-ttu-id="09b44-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="09b44-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="09b44-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="09b44-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="09b44-126">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="09b44-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="09b44-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="09b44-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
