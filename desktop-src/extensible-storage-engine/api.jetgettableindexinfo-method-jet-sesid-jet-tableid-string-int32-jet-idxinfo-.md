---
description: 'Altre informazioni su: metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)'
title: Metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100742
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc9c3432e34f36d13b2a12880118f2b5c36a8ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966910"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-int32-jet_idxinfo"></a><span data-ttu-id="a0c62-103">Metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="a0c62-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</span></span>

<span data-ttu-id="a0c62-104">Recupera informazioni sugli indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="a0c62-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="a0c62-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0c62-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0c62-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a0c62-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c62-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0c62-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As Integer
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out int result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="a0c62-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0c62-108">Parameters</span></span>

  - <span data-ttu-id="a0c62-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a0c62-109">sesid</span></span>  
    <span data-ttu-id="a0c62-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0c62-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a0c62-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a0c62-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0c62-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a0c62-112">tableid</span></span>  
    <span data-ttu-id="a0c62-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0c62-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a0c62-114">Tabella per cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="a0c62-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0c62-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="a0c62-115">indexname</span></span>  
    <span data-ttu-id="a0c62-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a0c62-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a0c62-117">Nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a0c62-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0c62-118">result</span><span class="sxs-lookup"><span data-stu-id="a0c62-118">result</span></span>  
    <span data-ttu-id="a0c62-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a0c62-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a0c62-120">Compilato con informazioni sugli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="a0c62-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0c62-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="a0c62-121">infoLevel</span></span>  
    <span data-ttu-id="a0c62-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a0c62-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="a0c62-123">Tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a0c62-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0c62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0c62-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0c62-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a0c62-125">Reference</span></span>

[<span data-ttu-id="a0c62-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="a0c62-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a0c62-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="a0c62-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a0c62-128">Overload JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a0c62-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="a0c62-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a0c62-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
