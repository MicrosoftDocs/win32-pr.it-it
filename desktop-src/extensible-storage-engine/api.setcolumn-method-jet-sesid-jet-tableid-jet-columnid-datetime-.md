---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.DateTime)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100875
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
ms.openlocfilehash: e43864a1b632adbc4ecf84d4963e7f87ea799283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305550"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-datetime"></a><span data-ttu-id="f99e8-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</span><span class="sxs-lookup"><span data-stu-id="f99e8-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</span></span>

<span data-ttu-id="f99e8-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="f99e8-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="f99e8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f99e8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f99e8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f99e8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f99e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f99e8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As DateTime _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DateTimeApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    DateTime data
)
```

#### <a name="parameters"></a><span data-ttu-id="f99e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f99e8-108">Parameters</span></span>

  - <span data-ttu-id="f99e8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f99e8-109">sesid</span></span>  
    <span data-ttu-id="f99e8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f99e8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f99e8-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f99e8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f99e8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f99e8-112">tableid</span></span>  
    <span data-ttu-id="f99e8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f99e8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f99e8-114">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f99e8-114">The cursor to update.</span></span> <span data-ttu-id="f99e8-115">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f99e8-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="f99e8-116">columnid</span><span class="sxs-lookup"><span data-stu-id="f99e8-116">columnid</span></span>  
    <span data-ttu-id="f99e8-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f99e8-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f99e8-118">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="f99e8-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="f99e8-119">data</span><span class="sxs-lookup"><span data-stu-id="f99e8-119">data</span></span>  
    <span data-ttu-id="f99e8-120">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="f99e8-120">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
    
    <span data-ttu-id="f99e8-121">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="f99e8-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="f99e8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f99e8-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f99e8-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f99e8-123">Reference</span></span>

[<span data-ttu-id="f99e8-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="f99e8-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f99e8-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="f99e8-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f99e8-126">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="f99e8-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="f99e8-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f99e8-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
