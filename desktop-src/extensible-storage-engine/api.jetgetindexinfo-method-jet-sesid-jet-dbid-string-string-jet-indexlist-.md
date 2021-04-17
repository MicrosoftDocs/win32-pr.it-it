---
description: 'Altre informazioni su: metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)'
title: Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
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
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306282"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="8640e-103">Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="8640e-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="8640e-104">**Nota: questa API è ora obsoleta.**</span><span class="sxs-lookup"><span data-stu-id="8640e-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="8640e-105">Recupera informazioni sugli indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="8640e-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="8640e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8640e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8640e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8640e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8640e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8640e-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="8640e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8640e-109">Parameters</span></span>

  - <span data-ttu-id="8640e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="8640e-110">sesid</span></span>  
    <span data-ttu-id="8640e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8640e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8640e-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8640e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8640e-113">dbid</span><span class="sxs-lookup"><span data-stu-id="8640e-113">dbid</span></span>  
    <span data-ttu-id="8640e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8640e-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8640e-115">Database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8640e-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8640e-116">tablename</span><span class="sxs-lookup"><span data-stu-id="8640e-116">tablename</span></span>  
    <span data-ttu-id="8640e-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8640e-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8640e-118">Nome della tabella in cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="8640e-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="8640e-119">Ignorato</span><span class="sxs-lookup"><span data-stu-id="8640e-119">ignored</span></span>  
    <span data-ttu-id="8640e-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8640e-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8640e-121">Questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8640e-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="8640e-122">elenco di indici</span><span class="sxs-lookup"><span data-stu-id="8640e-122">indexlist</span></span>  
    <span data-ttu-id="8640e-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="8640e-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="8640e-124">Compilato con informazioni sugli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="8640e-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="8640e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8640e-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8640e-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8640e-126">Reference</span></span>

[<span data-ttu-id="8640e-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="8640e-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8640e-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="8640e-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8640e-129">Overload JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="8640e-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="8640e-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8640e-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
