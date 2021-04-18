---
description: 'Altre informazioni su: metodo API. JetSetColumnDefaultValue'
title: API. JetSetColumnDefaultValue, metodo
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318828"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="5a4e3-103">API. JetSetColumnDefaultValue, metodo</span><span class="sxs-lookup"><span data-stu-id="5a4e3-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="5a4e3-104">Modifica il valore predefinito di una colonna esistente.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="5a4e3-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a4e3-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a4e3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5a4e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a4e3-108">Parameters</span></span>

  - <span data-ttu-id="5a4e3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5a4e3-109">sesid</span></span>  
    <span data-ttu-id="5a4e3-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5a4e3-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-112">dbid</span><span class="sxs-lookup"><span data-stu-id="5a4e3-112">dbid</span></span>  
    <span data-ttu-id="5a4e3-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5a4e3-114">Database contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-115">tableName</span><span class="sxs-lookup"><span data-stu-id="5a4e3-115">tableName</span></span>  
    <span data-ttu-id="5a4e3-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5a4e3-117">Nome della tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-118">columnName</span><span class="sxs-lookup"><span data-stu-id="5a4e3-118">columnName</span></span>  
    <span data-ttu-id="5a4e3-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5a4e3-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-121">data</span><span class="sxs-lookup"><span data-stu-id="5a4e3-121">data</span></span>  
    <span data-ttu-id="5a4e3-122">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="5a4e3-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="5a4e3-123">Nuovo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="5a4e3-124">dataSize</span></span>  
    <span data-ttu-id="5a4e3-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5a4e3-126">Dimensioni del nuovo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a4e3-127">grbit</span><span class="sxs-lookup"><span data-stu-id="5a4e3-127">grbit</span></span>  
    <span data-ttu-id="5a4e3-128">Tipo: [Microsoft. ISAM. esent. Interop. SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5a4e3-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5a4e3-129">Opzioni del valore predefinito della colonna.</span><span class="sxs-lookup"><span data-stu-id="5a4e3-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a4e3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a4e3-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a4e3-131">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5a4e3-131">Reference</span></span>

[<span data-ttu-id="5a4e3-132">Classe API</span><span class="sxs-lookup"><span data-stu-id="5a4e3-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5a4e3-133">Membri API</span><span class="sxs-lookup"><span data-stu-id="5a4e3-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5a4e3-134">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a4e3-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
