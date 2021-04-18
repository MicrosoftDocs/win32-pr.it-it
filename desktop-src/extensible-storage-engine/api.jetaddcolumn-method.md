---
description: 'Altre informazioni su: metodo API. JetAddColumn'
title: API. JetAddColumn, metodo
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306323"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="2774c-103">API. JetAddColumn, metodo</span><span class="sxs-lookup"><span data-stu-id="2774c-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="2774c-104">Consente di aggiungere una nuova colonna a una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="2774c-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="2774c-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2774c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2774c-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2774c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2774c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2774c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="2774c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2774c-108">Parameters</span></span>

  - <span data-ttu-id="2774c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2774c-109">sesid</span></span>  
    <span data-ttu-id="2774c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2774c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2774c-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2774c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="2774c-112">tableid</span></span>  
    <span data-ttu-id="2774c-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2774c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2774c-114">Tabella alla quale aggiungere la colonna.</span><span class="sxs-lookup"><span data-stu-id="2774c-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-115">colonna</span><span class="sxs-lookup"><span data-stu-id="2774c-115">column</span></span>  
    <span data-ttu-id="2774c-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2774c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2774c-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="2774c-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-118">columndef</span><span class="sxs-lookup"><span data-stu-id="2774c-118">columndef</span></span>  
    <span data-ttu-id="2774c-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="2774c-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="2774c-120">Definizione della colonna.</span><span class="sxs-lookup"><span data-stu-id="2774c-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="2774c-121">defaultValue</span></span>  
    <span data-ttu-id="2774c-122">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="2774c-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="2774c-123">Valore predefinito della colonna.</span><span class="sxs-lookup"><span data-stu-id="2774c-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-124">defaultValueSize</span><span class="sxs-lookup"><span data-stu-id="2774c-124">defaultValueSize</span></span>  
    <span data-ttu-id="2774c-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2774c-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2774c-126">Dimensioni del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2774c-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="2774c-127">columnid</span><span class="sxs-lookup"><span data-stu-id="2774c-127">columnid</span></span>  
    <span data-ttu-id="2774c-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2774c-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="2774c-129">Restituisce l'ColumnID della nuova colonna.</span><span class="sxs-lookup"><span data-stu-id="2774c-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="2774c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2774c-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2774c-131">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2774c-131">Reference</span></span>

[<span data-ttu-id="2774c-132">Classe API</span><span class="sxs-lookup"><span data-stu-id="2774c-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2774c-133">Membri API</span><span class="sxs-lookup"><span data-stu-id="2774c-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2774c-134">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2774c-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
