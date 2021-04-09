---
description: 'Altre informazioni su: metodo API. GetTableIndexes (JET_SESID, JET_DBID, stringa)'
title: Metodo API. GetTableIndexes (JET_SESID, JET_DBID, String)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878486"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="87ca5-103">Metodo API. GetTableIndexes (JET_SESID, JET_DBID, String)</span><span class="sxs-lookup"><span data-stu-id="87ca5-103">Api.GetTableIndexes method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="87ca5-104">Scorre tutti gli indici nella tabella, restituendo le informazioni su ognuna di esse.</span><span class="sxs-lookup"><span data-stu-id="87ca5-104">Iterates over all the indexs in the table, returning information about each one.</span></span>

<span data-ttu-id="87ca5-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87ca5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87ca5-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="87ca5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87ca5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87ca5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="87ca5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87ca5-108">Parameters</span></span>

  - <span data-ttu-id="87ca5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="87ca5-109">sesid</span></span>  
    <span data-ttu-id="87ca5-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87ca5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="87ca5-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="87ca5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="87ca5-112">dbid</span><span class="sxs-lookup"><span data-stu-id="87ca5-112">dbid</span></span>  
    <span data-ttu-id="87ca5-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87ca5-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="87ca5-114">Database contenente la tabella.</span><span class="sxs-lookup"><span data-stu-id="87ca5-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="87ca5-115">tablename</span><span class="sxs-lookup"><span data-stu-id="87ca5-115">tablename</span></span>  
    <span data-ttu-id="87ca5-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="87ca5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="87ca5-117">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="87ca5-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="87ca5-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87ca5-118">Return value</span></span>

<span data-ttu-id="87ca5-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="87ca5-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="87ca5-120">Iteratore su un IndexInfo per ogni indice nella tabella.</span><span class="sxs-lookup"><span data-stu-id="87ca5-120">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87ca5-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87ca5-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87ca5-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="87ca5-122">Reference</span></span>

[<span data-ttu-id="87ca5-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="87ca5-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="87ca5-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="87ca5-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="87ca5-125">Overload GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="87ca5-125">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="87ca5-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="87ca5-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
