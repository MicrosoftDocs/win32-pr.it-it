---
description: 'Altre informazioni su: metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)'
title: Metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128703"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="e5798-103">Metodo API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="e5798-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="e5798-104">Recupera le informazioni su una colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="e5798-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="e5798-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5798-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5798-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5798-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5798-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5798-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="e5798-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5798-108">Parameters</span></span>

  - <span data-ttu-id="e5798-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e5798-109">sesid</span></span>  
    <span data-ttu-id="e5798-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5798-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e5798-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e5798-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5798-112">dbid</span><span class="sxs-lookup"><span data-stu-id="e5798-112">dbid</span></span>  
    <span data-ttu-id="e5798-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5798-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e5798-114">Database che contiene la tabella.</span><span class="sxs-lookup"><span data-stu-id="e5798-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5798-115">tablename</span><span class="sxs-lookup"><span data-stu-id="e5798-115">tablename</span></span>  
    <span data-ttu-id="e5798-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e5798-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e5798-117">Nome della tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="e5798-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5798-118">columnName</span><span class="sxs-lookup"><span data-stu-id="e5798-118">columnName</span></span>  
    <span data-ttu-id="e5798-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e5798-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e5798-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="e5798-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5798-121">columndef</span><span class="sxs-lookup"><span data-stu-id="e5798-121">columndef</span></span>  
    <span data-ttu-id="e5798-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="e5798-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="e5798-123">Compilato con le informazioni sulla colonna.</span><span class="sxs-lookup"><span data-stu-id="e5798-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5798-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5798-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5798-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e5798-125">Reference</span></span>

[<span data-ttu-id="e5798-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="e5798-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e5798-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="e5798-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e5798-128">Overload JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="e5798-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="e5798-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e5798-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
