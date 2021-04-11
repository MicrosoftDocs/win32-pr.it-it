---
description: 'Altre informazioni su: metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)'
title: Metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
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
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226430"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="2d683-103">Metodo API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="2d683-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="2d683-104">**Nota: questa API è ora obsoleta.**</span><span class="sxs-lookup"><span data-stu-id="2d683-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="2d683-105">Recupera informazioni sugli indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="2d683-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="2d683-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d683-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d683-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d683-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d683-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d683-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="2d683-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d683-109">Parameters</span></span>

  - <span data-ttu-id="2d683-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2d683-110">sesid</span></span>  
    <span data-ttu-id="2d683-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2d683-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2d683-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2d683-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d683-113">TableID</span><span class="sxs-lookup"><span data-stu-id="2d683-113">tableid</span></span>  
    <span data-ttu-id="2d683-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2d683-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2d683-115">Tabella per cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="2d683-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d683-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="2d683-116">indexname</span></span>  
    <span data-ttu-id="2d683-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2d683-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2d683-118">Questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2d683-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d683-119">elenco di indici</span><span class="sxs-lookup"><span data-stu-id="2d683-119">indexlist</span></span>  
    <span data-ttu-id="2d683-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="2d683-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="2d683-121">Compilato con informazioni sugli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="2d683-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d683-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d683-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d683-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2d683-123">Reference</span></span>

[<span data-ttu-id="2d683-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="2d683-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2d683-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="2d683-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2d683-126">Overload JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="2d683-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="2d683-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2d683-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
