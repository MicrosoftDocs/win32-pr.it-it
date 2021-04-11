---
description: 'Altre informazioni su: metodo API. GetTableColumns (JET_SESID, JET_TABLEID)'
title: Metodo API. GetTableColumns (JET_SESID, JET_TABLEID)
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128070"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a><span data-ttu-id="d14a4-103">Metodo API. GetTableColumns (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="d14a4-103">Api.GetTableColumns method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="d14a4-104">Scorre tutte le colonne della tabella, restituendo le informazioni su ognuna di esse.</span><span class="sxs-lookup"><span data-stu-id="d14a4-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="d14a4-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d14a4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d14a4-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d14a4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d14a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d14a4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="d14a4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d14a4-108">Parameters</span></span>

  - <span data-ttu-id="d14a4-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d14a4-109">sesid</span></span>  
    <span data-ttu-id="d14a4-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d14a4-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d14a4-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d14a4-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d14a4-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d14a4-112">tableid</span></span>  
    <span data-ttu-id="d14a4-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d14a4-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d14a4-114">Tabella per cui recuperare le informazioni sulle colonne.</span><span class="sxs-lookup"><span data-stu-id="d14a4-114">The table to retrieve column information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d14a4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d14a4-115">Return value</span></span>

<span data-ttu-id="d14a4-116">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="d14a4-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="d14a4-117">Iteratore su ColumnInfo per ogni colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="d14a4-117">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d14a4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d14a4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d14a4-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d14a4-119">Reference</span></span>

[<span data-ttu-id="d14a4-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="d14a4-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d14a4-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="d14a4-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d14a4-122">Overload GetTableColumns</span><span class="sxs-lookup"><span data-stu-id="d14a4-122">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="d14a4-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d14a4-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
