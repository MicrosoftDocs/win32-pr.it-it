---
description: 'Altre informazioni su: metodo API. JetCreateTable'
title: API. JetCreateTable, metodo
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484540"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="8802c-103">API. JetCreateTable, metodo</span><span class="sxs-lookup"><span data-stu-id="8802c-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="8802c-104">Creare una tabella vuota.</span><span class="sxs-lookup"><span data-stu-id="8802c-104">Create an empty table.</span></span> <span data-ttu-id="8802c-105">La tabella appena creata viene aperta in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="8802c-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="8802c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8802c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8802c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8802c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8802c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8802c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="8802c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8802c-109">Parameters</span></span>

  - <span data-ttu-id="8802c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="8802c-110">sesid</span></span>  
    <span data-ttu-id="8802c-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8802c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8802c-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8802c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8802c-113">dbid</span><span class="sxs-lookup"><span data-stu-id="8802c-113">dbid</span></span>  
    <span data-ttu-id="8802c-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8802c-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8802c-115">Database in cui creare la tabella.</span><span class="sxs-lookup"><span data-stu-id="8802c-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="8802c-116">table</span><span class="sxs-lookup"><span data-stu-id="8802c-116">table</span></span>  
    <span data-ttu-id="8802c-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8802c-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8802c-118">Nome della tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="8802c-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="8802c-119">pagine</span><span class="sxs-lookup"><span data-stu-id="8802c-119">pages</span></span>  
    <span data-ttu-id="8802c-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8802c-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8802c-121">Numero iniziale di pagine nella tabella.</span><span class="sxs-lookup"><span data-stu-id="8802c-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="8802c-122">densità</span><span class="sxs-lookup"><span data-stu-id="8802c-122">density</span></span>  
    <span data-ttu-id="8802c-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8802c-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8802c-124">Densità predefinita della tabella.</span><span class="sxs-lookup"><span data-stu-id="8802c-124">The default density of the table.</span></span> <span data-ttu-id="8802c-125">Viene usato quando si esegue inserimenti sequenziali.</span><span class="sxs-lookup"><span data-stu-id="8802c-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="8802c-126">TableID</span><span class="sxs-lookup"><span data-stu-id="8802c-126">tableid</span></span>  
    <span data-ttu-id="8802c-127">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8802c-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8802c-128">Restituisce l'TableID della nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="8802c-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="8802c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8802c-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8802c-130">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8802c-130">Reference</span></span>

[<span data-ttu-id="8802c-131">Classe API</span><span class="sxs-lookup"><span data-stu-id="8802c-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8802c-132">Membri API</span><span class="sxs-lookup"><span data-stu-id="8802c-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8802c-133">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8802c-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
