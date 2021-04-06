---
description: 'Altre informazioni su: metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)'
title: Metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100730
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa120cf78001ed608a2385e07f388ae91bc9b425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758987"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-jet_columnid-jet_columndef"></a><span data-ttu-id="9ea79-103">Metodo API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="9ea79-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span></span>

<span data-ttu-id="9ea79-104">Recupera le informazioni su una colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="9ea79-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="9ea79-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ea79-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9ea79-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ea79-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea79-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ea79-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnid, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="9ea79-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ea79-108">Parameters</span></span>

  - <span data-ttu-id="9ea79-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9ea79-109">sesid</span></span>  
    <span data-ttu-id="9ea79-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9ea79-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9ea79-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="9ea79-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ea79-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9ea79-112">tableid</span></span>  
    <span data-ttu-id="9ea79-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9ea79-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9ea79-114">Tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="9ea79-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ea79-115">columnid</span><span class="sxs-lookup"><span data-stu-id="9ea79-115">columnid</span></span>  
    <span data-ttu-id="9ea79-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9ea79-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9ea79-117">ColumnID della colonna.</span><span class="sxs-lookup"><span data-stu-id="9ea79-117">The columnid of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ea79-118">columndef</span><span class="sxs-lookup"><span data-stu-id="9ea79-118">columndef</span></span>  
    <span data-ttu-id="9ea79-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="9ea79-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="9ea79-120">Compilato con le informazioni sulla colonna.</span><span class="sxs-lookup"><span data-stu-id="9ea79-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ea79-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ea79-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ea79-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9ea79-122">Reference</span></span>

[<span data-ttu-id="9ea79-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="9ea79-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9ea79-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="9ea79-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9ea79-125">Overload JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="9ea79-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="9ea79-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9ea79-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
