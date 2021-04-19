---
description: 'Altre informazioni su: metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)'
title: Metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306294"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a><span data-ttu-id="bd81d-103">Metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="bd81d-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="bd81d-104">Recupera informazioni su tutte le colonne di una tabella.</span><span class="sxs-lookup"><span data-stu-id="bd81d-104">Retrieves information about all columns in a table.</span></span>

<span data-ttu-id="bd81d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bd81d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bd81d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bd81d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bd81d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd81d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="bd81d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd81d-108">Parameters</span></span>

  - <span data-ttu-id="bd81d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="bd81d-109">sesid</span></span>  
    <span data-ttu-id="bd81d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bd81d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bd81d-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="bd81d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd81d-112">dbid</span><span class="sxs-lookup"><span data-stu-id="bd81d-112">dbid</span></span>  
    <span data-ttu-id="bd81d-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bd81d-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="bd81d-114">Database che contiene la tabella.</span><span class="sxs-lookup"><span data-stu-id="bd81d-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd81d-115">tablename</span><span class="sxs-lookup"><span data-stu-id="bd81d-115">tablename</span></span>  
    <span data-ttu-id="bd81d-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bd81d-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bd81d-117">Nome della tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="bd81d-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd81d-118">columnName</span><span class="sxs-lookup"><span data-stu-id="bd81d-118">columnName</span></span>  
    <span data-ttu-id="bd81d-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bd81d-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bd81d-120">Questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bd81d-120">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd81d-121">istogramma</span><span class="sxs-lookup"><span data-stu-id="bd81d-121">columnlist</span></span>  
    <span data-ttu-id="bd81d-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="bd81d-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="bd81d-123">Compilato con informazioni sulle colonne della tabella.</span><span class="sxs-lookup"><span data-stu-id="bd81d-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd81d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd81d-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bd81d-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bd81d-125">Reference</span></span>

[<span data-ttu-id="bd81d-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="bd81d-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bd81d-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="bd81d-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bd81d-128">Overload JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="bd81d-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="bd81d-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bd81d-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
