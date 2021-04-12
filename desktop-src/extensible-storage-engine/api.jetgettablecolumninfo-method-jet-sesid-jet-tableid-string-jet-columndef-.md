---
description: 'Altre informazioni su: metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)'
title: Metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100724
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60e984fdb1577dc69a352c327c1af605e0d441d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344251"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columndef"></a><span data-ttu-id="53cd1-103">Metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="53cd1-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="53cd1-104">Recupera le informazioni su una colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="53cd1-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="53cd1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53cd1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53cd1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53cd1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53cd1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53cd1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="53cd1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53cd1-108">Parameters</span></span>

  - <span data-ttu-id="53cd1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="53cd1-109">sesid</span></span>  
    <span data-ttu-id="53cd1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53cd1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="53cd1-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="53cd1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="53cd1-112">TableID</span><span class="sxs-lookup"><span data-stu-id="53cd1-112">tableid</span></span>  
    <span data-ttu-id="53cd1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53cd1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="53cd1-114">Tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="53cd1-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="53cd1-115">columnName</span><span class="sxs-lookup"><span data-stu-id="53cd1-115">columnName</span></span>  
    <span data-ttu-id="53cd1-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="53cd1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="53cd1-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="53cd1-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="53cd1-118">columndef</span><span class="sxs-lookup"><span data-stu-id="53cd1-118">columndef</span></span>  
    <span data-ttu-id="53cd1-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="53cd1-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="53cd1-120">Compilato con le informazioni sulla colonna.</span><span class="sxs-lookup"><span data-stu-id="53cd1-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="53cd1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53cd1-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53cd1-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53cd1-122">Reference</span></span>

[<span data-ttu-id="53cd1-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="53cd1-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="53cd1-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="53cd1-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="53cd1-125">Overload JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="53cd1-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="53cd1-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53cd1-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
