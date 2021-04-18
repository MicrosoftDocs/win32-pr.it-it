---
description: 'Altre informazioni su: metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)'
title: Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100769
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eed2ba4a3f578dda966b2b4530f26de25089681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306281"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-string-jet_idxinfo"></a><span data-ttu-id="32802-103">Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="32802-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="32802-104">Recupera informazioni sugli indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="32802-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="32802-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32802-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32802-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="32802-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32802-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32802-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="32802-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="32802-108">Parameters</span></span>

  - <span data-ttu-id="32802-109">sesid</span><span class="sxs-lookup"><span data-stu-id="32802-109">sesid</span></span>  
    <span data-ttu-id="32802-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32802-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="32802-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="32802-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="32802-112">dbid</span><span class="sxs-lookup"><span data-stu-id="32802-112">dbid</span></span>  
    <span data-ttu-id="32802-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32802-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="32802-114">Database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="32802-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="32802-115">tablename</span><span class="sxs-lookup"><span data-stu-id="32802-115">tablename</span></span>  
    <span data-ttu-id="32802-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="32802-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="32802-117">Nome della tabella in cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="32802-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="32802-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="32802-118">indexname</span></span>  
    <span data-ttu-id="32802-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="32802-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="32802-120">Nome dell'indice per il quale recuperare informazioni.</span><span class="sxs-lookup"><span data-stu-id="32802-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="32802-121">result</span><span class="sxs-lookup"><span data-stu-id="32802-121">result</span></span>  
    <span data-ttu-id="32802-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="32802-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="32802-123">Compilato con informazioni sugli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="32802-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="32802-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="32802-124">infoLevel</span></span>  
    <span data-ttu-id="32802-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="32802-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="32802-126">Tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="32802-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="32802-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32802-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32802-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="32802-128">Reference</span></span>

[<span data-ttu-id="32802-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="32802-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="32802-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="32802-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="32802-131">Overload JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="32802-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="32802-132">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="32802-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
